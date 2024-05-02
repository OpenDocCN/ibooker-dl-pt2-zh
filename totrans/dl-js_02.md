## 致谢

本书的整体结构要感谢 François Chollet 的《Python 深度学习》。尽管代码是用不同的语言重写的，并且为 JavaScript 生态系统添加了许多新内容，以反映该领域的新发展，但没有 François 领导的 Keras 的先驱工作，无论是这本书还是 TensorFlow.js 的整个高级 API 都不可能成为现实。

我们完成这本书和所有相关代码的旅程愉快而充实，这要归功于我们在谷歌的 TensorFlow.js 团队的不可思议的支持。Daniel Smilkov 和 Nikhil Thorat 在低级别 WebGL 内核和反向传播方面的开创性和基础性工作为模型构建和训练打下了坚实的基础。Nick Kreeger 对 TensorFlow 的 C 库进行 Node.js 绑定的工作是我们能够在浏览器和 Node.js 中使用相同代码运行神经网络的主要原因。David Soergel 和 Kangyi Zhang 开发的 TensorFlow.js 数据 API 使得本书的 第六章 成为可能，而 第七章 则得益于 Yannick Assogba 的可视化工作。在 第十一章 中描述的性能优化技术，没有 Ping Yu 在 TensorFlow 的操作级接口方面的工作就不可能实现。我们示例的速度如果没有 Ann Yuan 的专注性能优化工作，今天的速度不可能如此之快。Sarah Sirajuddin、Sandeep Gupta 和 Brijesh Krishnaswami 的领导对 TensorFlow.js 项目的整体长期成功至关重要。

如果没有 D. Sculley 的支持和鼓励，我们就会偏离轨道。我们也非常感谢来自谷歌的 Fernanda Viegas、Martin Wattenberg、Hal Abelson 和我们许多其他同事的所有鼓励。我们的写作和内容在 François Chollet、Nikhil Thorat、Daniel Smilkov、Jamie Smith、Brian K. Lee 和 Augustus Odena 的详细审查以及与 Suharsh Sivakumar 的深入讨论的结果下得到了极大的改善。

在像 TensorFlow.js 这样的项目上工作的独特乐趣之一是有机会与全球开源软件社区一起工作并互动。TensorFlow.js 很幸运地拥有一群才华横溢、积极向上的贡献者，包括 Manraj Singh、Kai Sasaki、Josh Gartman、Sasha Illarionov、David Sanders、syt123450@，以及许多其他不懈努力的人，他们对库的不懈工作扩展了其功能并提高了其质量。Manraj Singh 还为本书的 第三章 贡献了用于示例的钓鱼检测示例。

我们要感谢 Manning 出版社的编辑团队。Brian Sawyer、Jennifer Stout，Rebecca Rinehart 和 Mehmed Pasic 等众多人员的专注和不懈工作，使我们作者得以专注于写作内容。Marc-Philip Huget 在整个开发过程中提供了广泛而深刻的技术审查。特别感谢我们的评论者(排名不分先后)：Alain Lompo、Andreas Refsgaard、Buu Nguyen、David DiMaria、Edin Kapic、Edwin Kwok、Eoghan O'Donnell、Evan Wallace、George Thomas、Giuliano Bertoti、Jason Hales、Marcio Nicolau、Michael Wall、Paulo Nuin、Pietro Maffi、Polina Keselman、Prabhuti Prakash、Ryan Burrows、Satej Sahu、Suresh Rangarajulu、Ursin Stauss 和 Vaijanath Rao，他们的建议使这本书更加优秀。

我们感谢 MEAP 的读者指出其中不少排版和技术错误。

最后，没有我们家人的巨大理解和牺牲，这一切将不可能。Shanqing Cai 想向他的妻子 Wei，以及他的父母和岳父岳母表示最深的感谢，在这本书的一年写作过程中提供了帮助和支持。Stan Bileschi 要感谢他的母亲和父亲，以及他的继母和继父，为他在科学和工程领域建立了成功的职业生涯奠定了基础和方向。他也要感谢他的妻子 Constance 的爱和支持。Eric Nielsen 要感谢他的朋友和家人，谢谢你们。
