## 第二十二章：B.3\. TensorFlow.js 中的内存管理：`tf.dispose()`和`tf.tidy()`

在 TensorFlow.js 中，如果你直接处理张量对象，你需要对它们执行内存管理。特别是在创建和使用张量后，张量需要被释放，否则它将继续占用分配给它的内存。如果未释放的张量数量过多或者总大小过大，它们最终将导致浏览器标签页耗尽 WebGL 内存或导致 Node.js 进程耗尽系统或 GPU 内存（取决于是否使用 tfjs-node 的 CPU 或 GPU 版本）。TensorFlow.js 不会自动对用户创建的张量进行垃圾回收。[[5]](#app02fn5) 这是因为 JavaScript 不支持对象终结。TensorFlow.js 提供了两个内存管理函数：`tf.dispose()`和`tf.tidy()`。

> ⁵
> 
> 然而，在 TensorFlow.js 函数和对象方法中创建的张量由库本身管理，因此你不需要担心在调用这些函数或方法时包装它们在`tf.tidy()`中。其中的示例函数包括`tf.confusionMatrix()`、`tf.Model.predict()`和`tf.Model.fit()`。

例如，考虑使用`for`循环对 TensorFlow.js 模型进行重复推理的示例：

```js
const model = await tf.loadLayersModel(                                    ***1***
    'https://storage.googleapis.com/tfjs-models/tfjs/iris_v1/model.json'); ***1***
const x = tf.randomUniform([1, 4]);                                        ***2***
for (let i = 0; i < 3; ++i) {
  const y = model.predict(x);
  y.print();
  console.log(`# of tensors: ${tf.memory().numTensors}` );                 ***3***
}
```

+   ***1*** 从网络上加载预先训练好的模型

+   ***2*** 创建一个虚拟输入张量

+   ***3*** 检查当前已分配张量的数量

输出将如下所示

```js
Tensor
     [[0.4286409, 0.4692867, 0.1020722],]
# of tensors: 14
Tensor
     [[0.4286409, 0.4692867, 0.1020722],]
# of tensors: 15
Tensor
     [[0.4286409, 0.4692867, 0.1020722],]
# of tensors: 16
```

正如你在控制台日志中看到的那样，每次调用`model.predict()`都会生成一个额外的张量，在迭代结束后不会被释放。如果允许`for`循环运行足够数量的迭代，它最终会导致内存不足错误。这是因为输出张量`y`没有被正确释放，导致张量内存泄漏。有两种方法可以修复这个内存泄漏。

在第一种方法中，你可以在不再需要输出张量时调用`tf.dispose()`：

```js
for (let i = 0; i < 3; ++i) {
  const y = model.predict(x);
  y.print();
  tf.dispose(y);                                          ***1***
  console.log(`# of tensors: ${tf.memory().numTensors}` );
}
```

+   ***1*** 在使用后释放输出张量

在第二种方法中，你可以在`for`循环的主体部分使用`tf.tidy()`：

```js
for (let i = 0; i < 3; ++i) {
  tf.tidy(() => {                          ***1***
    const y = model.predict(x);
    y.print();
    console.log(`# of tensors: ${tf.memory().numTensors}` );
  });
}
```

+   ***1*** `tf.tidy()`自动释放传递给它的函数中创建的所有张量，除了由该函数返回的张量。

无论选用哪种方法，你应该看到迭代中分配的张量数量变为常数，表明不再有张量内存泄漏。哪种方法应该优先使用呢？通常，你应该使用`tf.tidy()`（第二种方法），因为它消除了跟踪需要释放哪些张量的需要。`tf.tidy()`是一个智能函数，它释放传递给它的匿名函数中创建的所有张量（除了由该函数返回的张量-稍后再说），即使这些张量没有绑定到任何 JavaScript 对象。例如，假设我们稍微修改先前的推理代码，以便使用`argMax()`获得获胜类别的索引：

```js
const model = await tf.loadLayersModel(
    'https://storage.googleapis.com/tfjs-models/tfjs/iris_v1/model.json');
const x = tf.randomUniform([1, 4]);
for (let i = 0; i < 3; ++i) {
  const winningIndex =
           model.predict(x).argMax().dataSync()[0];
  console.log(`winning index: ${winningIndex}`);
  console.log(`# of tensors: ${tf.memory().numTensors}` );
}
```

当这段代码运行时，你会发现它每次迭代泄漏两个张量：

```js
winning index: 0
# of tensors: 15
winning index: 0
# of tensors: 17
winning index: 0
# of tensors: 19
```

为什么每次迭代泄漏两个张量？因为这行代码：

```js
   const winningIndex =
       model.predict(x).argMax().dataSync()[0];
```

生成两个新的张量。第一个是`model.predict()`的输出，第二个是`argMax()`的返回值。这两个张量都没有绑定到任何 JavaScript 对象上。它们被创建后立即使用。这两个张量在某种意义上“丢失”——没有 JavaScript 对象可供您用来引用它们。因此，`tf.dispose()`不能用于清理这两个张量。但是，`tf.tidy()`仍然可以用来修复内存泄漏，因为它会对新张量执行簿记，无论它们是否绑定到 JavaScript 对象上：

```js
const model = await tf.loadLayersModel(
    'https://storage.googleapis.com/tfjs-models/tfjs/iris_v1/model.json');
const x = tf.randomUniform([1, 4]);
for (let i = 0; i < 3; ++i) {
  tf.tidy(() => {                                                  ***1***
    const winningIndex = model.predict(x).argMax().dataSync()[0];
    console.log(`winning index: ${winningIndex}`);
    console.log(`# of tensors: ${tf.memory().numTensors}` );       ***1***
  });
}
```

+   ***1*** `tf.tidy()`会自动处理传递给它作为参数的匿名函数中创建的张量，即使这些张量没有绑定到 JavaScript 对象上。

`tf.tidy()`的示例用法操作的是不返回任何张量的函数。如果该函数返回张量，则不希望将它们处理掉，因为它们需要在后续使用。这种情况在使用 TensorFlow.js 提供的基本张量操作编写自定义张量操作时经常遇到。例如，假设我们想编写一个函数来计算输入张量的标准化值——即，减去平均值并将标准差缩放为 1 的张量：

```js
function normalize(x) {
  const mean = x.mean();
  const sd = x.norm(2);
  return x.sub(mean).div(sd);
}
```

这个实现有什么问题？^([6]) 就内存管理而言，它泄漏了三个张量：1）均值，2）SD 和 3）一个更微妙的泄漏：`sub()`调用的返回值。为了修复内存泄漏问题，我们将函数体包装在`tf.tidy()`中：

> ⁶
> 
> 这个实现还有其他问题。例如，它没有对输入张量进行健全性检查，以确保它至少有两个元素，使 SD 不为零，否则将导致除以零和无限结果。但是这些问题与此处的讨论无直接关联。

```js
function normalize(x) {
  return tf.tidy(() => {
    const mean = x.mean();
    const sd = x.norm(2);
    return x.sub(mean).div(sd);
       });
}
```

在这里，`tf.tidy()`为我们完成了三个操作：

+   它会自动处理在匿名函数中创建但未被它返回的张量，包括之前提到的所有泄漏。我们在之前的例子中已经看到这一点了。

+   它检测到`div()`调用的输出由匿名函数返回，因此将其转发到自己的返回值。

+   在此期间，它将避免处理该特定张量，以便它可以在`tf.tidy()`调用之外使用。

如我们所见，`tf.tidy()` 是一种智能而强大的内存管理函数。它在 TensorFlow.js 代码库中被广泛使用。在本书的示例中，您还将经常看到它。然而，它有以下重要限制：作为参数传递给 `tf.tidy()` 的匿名函数 *不* 能是异步的。如果您有一些需要内存管理的异步代码，您应该使用 `tf.dispose()` 并手动跟踪待处理的张量。在这种情况下，您可以使用 `tf.memory().numTensor` 来检查泄漏张量的数量。一个好的做法是编写单元测试来断言不存在内存泄漏。
