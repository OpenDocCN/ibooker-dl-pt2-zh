## 前言 1

当我们开始使用 TensorFlow.js（TF.js）时，原名为 deeplearn.js，机器学习（ML）主要使用 Python 进行。作为 Google Brain 团队的 JavaScript 开发人员和 ML 实践者，我们很快意识到有机会链接这两个世界。如今，TF.js 已经赋予了广大 JavaScript 社区的新一波开发者创建和部署 ML 模型的能力，并启用了新的设备上计算的类别。

如果没有 Shanqing、Stan 和 Eric 对 TensorFlow Python 的贡献，包括 TensorFlow 调试器、即时执行以及构建和测试基础设施，TF.js 今天的形式将不会存在，他们独特地将 Python 和 JavaScript 两个世界联系在一起。在开发的早期阶段，他们的团队意识到 deeplearn.js 上需要一个库，该库可以提供高级构建模块来开发 ML 模型。Shanqing、Stan 和 Eric 等人构建了 TF.js Layers，使得可以将 Keras 模型转换为 JavaScript，并大大增加了 TF.js 生态系统中可用模型的数量。当 TF.js Layers 准备好时，我们向全世界发布了 TF.js。

为了调查软件开发人员的动机、障碍和需求，Carrie Cai 和 Philip Guo 在 TF.js 网站上发布了一项调查。这本书是对该研究摘要的直接回应：“我们的分析发现，开发人员对于 ML 框架的需求远远超过了只是想要在 API 方面得到帮助：更根本地，他们希望了解和应用 ML 本身的概念支持。” ^([1])

> ¹
> 
> C. Cai 和 P. Guo，（2019）“软件开发人员学习机器学习：动机、障碍和需求”，《IEEE 可视化语言和人本计算研讨会》，2019 年。

《JavaScript 深度学习》包含了深度学习理论和使用 TF.js 编写的 JavaScript 的实际示例。对于没有 ML 经验或正规数学背景的 JavaScript 开发人员来说，它是一个很好的资源，也可以帮助 ML 实践者将他们的工作拓展到 JavaScript 生态系统。这本书遵循《Python 深度学习》的模板，这是一本最受欢迎的应用 ML 文本之一，由 Keras 的创始人 François Chollet 编写。《JavaScript 深度学习》在扩展 Chollet 的工作方面做得非常出色，它充分利用了 JavaScript 的独特优势：互动性、可移植性和设备上计算。它涵盖了核心 ML 概念，并且不回避最先进的 ML 主题，例如文本翻译、生成模型和强化学习。它甚至还提供了在实际应用程序中部署 ML 模型的务实建议，这些建议是由具有丰富的实际经验的实践者撰写的。本书的示例使用交互式演示来展示 JavaScript 生态系统的独特优势。所有的代码都是开源的，因此您可以在线与其进行交互并进行分叉。

这本书应该成为那些想学习 ML 并将 JavaScript 作为他们的主要语言的读者的权威来源。作为 ML 和 JavaScript 的前沿，我们希望您发现本书中的概念有用，并且在 JavaScript ML 的旅程中收获丰富和令人兴奋的经验。

—NIKHIL THORAT 和 DANIEL SMILKOV，

deeplearn.js 的发明者

以及 TensorFlow.js 的技术负责人
