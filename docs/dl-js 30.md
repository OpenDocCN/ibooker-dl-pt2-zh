## B.4\. 计算梯度

这一部分适用于对在 TensorFlow.js 中执行导数和梯度计算感兴趣的读者。对于本书中的大多数深度学习模型，导数和梯度的计算都是在`model.fit()`和`model.fitDataset()`中自动完成的。然而，对于某些问题类型，比如在第七章中找到卷积滤波器的最大激活图像和在第十一章中的 RL，需要显式地计算导数和梯度。TensorFlow.js 提供了支持此类用例的 API。让我们从最简单的情景开始，即一个接受单个输入张量并返回单个输出张量的函数：

```js
const f = x => tf.atan(x);
```

为了计算函数(`f`)相对于输入(`x`)的导数，我们使用`tf.grad()`函数：

```js
const df = tf.grad(f);
```

注意，`tf.grad()`不会立即给出导数的值。相反，它会给出一个*函数*，即原始函数(`f`)的导数。您可以使用具体的`x`值调用该函数(`df`)，这时您就会得到`df/dx`的值。例如，

```js
const x = tf.tensor([-4, -2, 0, 2, 4]);
df(x).print();
```

它给出了一个输出，正确反映了在 x 值为-4、-2、0、2 和 4 时`atan()`函数的导数（参见图 B.5）：

```js
Tensor
    [0.0588235, 0.2, 1, 0.2, 0.0588235]
```

##### 图 B.5\. 函数`atan(x)`的图表

![](img/btab05_alt.jpg)

`tf.grad()`仅适用于具有单个输入张量的函数。如果您有一个具有多个输入的函数怎么办？让我们考虑一个简单的例子`h(x, y)`，它只是两个张量的乘积：

```js
const h = (x, y) => x.mul(y);
```

`tf.grads()`（带有名称中的“s”）生成一个函数，该函数返回输入函数相对于所有参数的偏导数：

```js
const dh = tf.grads(h);
const dhValues = dh([tf.tensor1d([1, 2]), tf.tensor1d([-1, -2])]);
dhValues[0].print();
dhValues[1].print();
```

这给出了结果

```js
Tensor
    [-1, -2]
Tensor
    [1, 2]
```

这些结果是正确的，因为相对于*x*的偏导数`*`*y*是*y*，相对于*y*的偏导数是*x*。

由`tf.grad()`和`tf.grads()`生成的函数只给出导数，而不是原始函数的返回值。在*h*(*x*, *y*)的示例中，如果我们不仅想要得到导数，还想要*h*的值，那么可以使用`tf.valueAndGrads()`函数：

```js
const vdh = tf.valueAndGrads(h);
const out = vdh([tf.tensor1d([1, 2]), tf.tensor1d([-1, -2])]);
```

输出(`out`)是一个具有两个字段的对象：`value`，即给定输入值时*h*的值，以及`grads`，其格式与由`tf.grads()`生成的函数的返回值相同，即偏导数张量的数组：

```js
out.value.print();
out.grads[0].print();
out.grads[1].print();

Tensor
    [-1, -4]
Tensor
    [-1, -2]
Tensor
    [1, 2]
```

讨论的 API 都涉及到计算函数相对于其显式参数的导数。然而，在深度学习中的一个常见情景是函数在计算中使用了权重。这些权重表示为 `tf.Variable` 对象，并且*不*作为参数明确传递给函数。对于这样的函数，我们经常需要在训练过程中计算相对于权重的导数。`tf.variableGrads()` 函数就是为此工作流程提供支持的，它跟踪被求导函数所访问的可训练变量，并自动计算相对于它们的导数。考虑以下示例：

```js
const trainable = true;
const a = tf.variable(tf.tensor1d([3, 4]), trainable, 'a');
const b = tf.variable(tf.tensor1d([5, 6]), trainable, 'b');
const x = tf.tensor1d([1, 2]);

const f = () => a.mul(x.square()).add(b.mul(x)).sum();     ***1***
const {value, grads} = tf.variableGrads(f);
```

+   ***1*** *f*(*a*, *b*) = *a* * *x* ^ 2 + *b* * *x*。调用 `sum()` 方法是因为 `tf.variableGrads()` 要求被求导函数返回一个标量。

`tf.variableGrads()` 的输出中的 `value` 字段是在给定 `a`、`b` 和 `x` 的当前值时 `f` 的返回值。 `grads` 字段是一个 JavaScript 对象，它在相应的键名下携带了对两个变量（`a` 和 `b`）的导数。例如，`f(a, b)` 关于 `a` 的导数是 `x ^ 2`，`f(a, b)` 关于 `b` 的导数是 `x`，

```js
grads.a.print();
grads.b.print();
```

这正确给出了

```js
Tensor
    [1, 4]
Tensor
    [1, 2]
```
