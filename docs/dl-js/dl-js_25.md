## 第十九章：A.2\. 在 Windows 上安装 tfjs-node-gpu

1.  确保您的 Windows 符合 CUDA Toolkit 的系统要求。某些 Windows 版本和 32 位机器架构不受 CUDA Toolkit 的支持。有关更多详情，请参阅 [`docs.nvidia.com/cuda/cuda-installation-guide-microsoft-windows/index.html#system-requirements`](https://docs.nvidia.com/cuda/cuda-installation-guide-microsoft-windows/index.html#system-requirements)。

1.  我们假设您已在系统上安装了 Node.js 和 npm，并且 Node.js 和 npm 的路径在您系统的环境变量 `Path` 中可用。如果没有，请访问 [`nodejs.org/en/download/`](https://nodejs.org/en/download/) 下载安装程序。

1.  安装 Microsoft Visual Studio，因为它是安装 CUDA Toolkit 所必需的。请参阅步骤 1 中相同的链接，以了解应安装哪个版本的 Visual Studio。

1.  下载并安装 Windows 版 CUDA Toolkit。在撰写本文时，运行 tfjs-node-gpu 需要 CUDA 10.0（最新版本：1.2.10）。请务必为您的 Windows 发行版选择正确的安装程序。支持 Windows 7 和 Windows 10 的安装程序。此步骤需要管理员权限。

1.  下载 CuDNN。确保 CuDNN 的版本与 CUDA 的版本匹配。例如，CuDNN 7.6 与 CUDA Toolkit 10.0 匹配。在下载 CuDNN 之前，NVIDIA 可能要求您在其网站上创建帐户并回答一些调查问题。

1.  与 CUDA Toolkit 安装程序不同，您刚下载的 CuDNN 是一个压缩文件。解压它，您将看到其中有三个文件夹：cuda/bin、cuda/include 和 cuda/lib/x64。找到 CUDA Toolkit 安装的目录（默认情况下，它类似于 C:/Program Files/NVIDIA CUDA Toolkit 10.0/cuda）。将解压后的文件复制到那里相应名称的子文件夹中。例如，解压的 zip 存档中的 cuda/bin 中的文件应复制到 C:/Program Files/NVIDIA CUDA Toolkit 10.0/cuda/bin。此步骤可能还需要管理员权限。

1.  安装 CUDA Toolkit 和 CuDNN 后，请重新启动 Windows 系统。我们发现这对于所有新安装的库都能正确加载以供 tfjs-node-gpu 使用是必要的。

1.  安装 npm 包 `window-build-tools`。这是下一步安装 npm 包 `@tensorflow/tfjs-node-gpu` 所必需的：

    ```js
    npm install --add-python-to-path='true' --global windows-build-tools
    ```

1.  使用 npm 安装包 `@tensorflow/tfjs` 和 `@tensorflow/tfjs-node-gpu`：

    ```js
    npm -i @tensorflow/tfjs @tensorflow/tfjs-node-gpu
    ```

1.  要验证安装是否成功，请打开节点命令行并运行

    ```js
    > const tf = require('@tensorflow/tfjs');
    > require('@tensorflow/tfjs-node-gpu');
    ```

    确保这两个命令都能顺利完成。在第二个命令之后，您应该在控制台中看到一些由 TensorFlow GPU 共享库打印的日志行。这些行将列出 tfjs-node-gpu 已识别并将在后续深度学习程序中使用的 CUDA 启用的 GPU 的详细信息。
