# 第三部分。将贝叶斯优化扩展到专门的设置

我们学习到的贝叶斯优化循环代表了广泛的优化问题。然而，现实生活场景通常不遵循这种高度理想化的模型。如果您可以同时运行多个函数评估，这在多 GPU 可用的超参数调整应用中很常见，会怎样？如果您有多个竞争的目标，您想要优化？本部分介绍了您可能在现实世界中遇到的一些最常见的优化情景，并讨论了如何将贝叶斯优化扩展到这些情景中。

为了增加吞吐量，许多设置允许实验并行运行。第七章介绍了批量贝叶斯优化框架，在这种框架中进行函数评估是批量进行的。我们学习如何扩展第二部分学到的决策策略到这个设置中，同时确保充分利用系统的并行性。

在关键安全用例中，我们不能自由地探索搜索空间，因为某些函数评估可能会产生有害效果。这促使出现了在所讨论的函数应如何行为上存在约束，并且在优化策略的设计中需要考虑这些约束的情况。第八章处理了这种情境，称为受限制的优化，并开发了必要的机制来应用贝叶斯优化。

第九章探讨了我们可以以不同成本和精度水平观察函数值的多种方式的情境；这通常被称为多信度贝叶斯优化。我们讨论了熵的自然扩展，以量化在不同保真度水平上进行评估的价值，并将该算法应用于平衡信息和成本。

已经证明，两两比较比数字评估或评分更准确地反映了一个人的偏好，因为它们更简单，对标注者的认知负荷更轻。第十章将贝叶斯优化应用于这种情境，首先使用特殊的 GP 模型，然后修改现有策略以适应这种两两比较工作流程。

多目标优化是一个常见的用例，我们旨在同时优化多个可能存在冲突的目标。我们研究了多目标优化问题，并开发了一个可以共同优化我们的多个目标的贝叶斯优化解决方案。

在这一系列特殊的优化设置中，有一个共同的主题：在考虑问题的结构时权衡探索和利用。通过看到在本部分如何将贝叶斯优化应用于各种设置中，我们不仅巩固了对这一技术的理解，而且使该技术在实际场景中更加适用。这些章节中开发的代码将帮助您立即解决您在现实生活中可能遇到的任何优化问题。