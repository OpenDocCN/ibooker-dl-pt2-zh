# 前言

GPT-3，或称为生成式预训练转换器 3，是由 OpenAI 开发的基于转换器的大型语言模型。它由惊人的 1750 亿参数组成。任何人都可以通过 OpenAI API 访问这个大型语言模型，这是一个简单易用的“文本输入、文本输出”用户界面，不需要任何技术先决条件。这是历史上第一次将像 GPT-3 这样的大型 AI 模型远程托管并提供给普通大众，只需简单的 API 调用。这种新的访问模式称为*模型即服务*。由于这种前所未有的访问方式，包括本书作者在内的许多人认为 GPT-3 是向人工智能（AI）民主化迈出的第一步。

随着 GPT-3 的推出，构建 AI 应用比以往任何时候都更容易。本书将向您展示如何轻松使用 OpenAI API 入门。此外，我们还将向您介绍利用此工具解决您的用例的创新方法。我们将审视建立在 GPT-3 之上的成功初创企业以及在其产品领域利用它的企业，并研究其发展中的问题和潜在未来趋势。

本书面向所有背景的人，而不仅仅是技术专业人士。如果您是以下人士，本书对您应该很有用：

+   一个希望在 AI 领域获得技能的数据专业人士

+   一位希望在 AI 领域建立下一个大项目的企业家

+   一位企业领袖，希望升级他们的 AI 知识并将其用于推动关键决策

+   一个作家、播客、社交媒体管理员或其他使用语言的创作者，希望利用 GPT-3 的语言能力进行创意工作

+   任何一个 AI 创意，曾经似乎在技术上不可能或者成本过高而被忽略的人

本书的第一部分涵盖了 OpenAI API 的基础知识。在书的第二部分，我们探索了围绕 GPT-3 自然形成的丰富生态系统。

第一章概述了在这些主题中移动所需的上下文和基本定义。在第二章中，我们深入探讨了 API，将其分解为最重要的元素，如引擎和端点，描述了它们的目的以及希望与之更深层次交互的读者的最佳实践。第三章为您的第一个 GPT-3 动力应用提供了一个简单而有趣的配方。

接下来，将焦点转移到令人兴奋的人工智能生态系统，在第四章中，我们采访了一些最成功的基于 GPT-3 的产品和应用的创始人，了解他们在商业规模上与模型互动的经历和挑战。第五章 着眼于企业如何看待 GPT-3 及其采用潜力。我们在第六章讨论了更广泛采用 GPT-3 的问题，如误用和偏见，以及解决这些问题的进展。最后，在第七章 中，我们展望未来，为您介绍 GPT-3 在更广泛的商业生态系统中定位时所带来的最令人兴奋的趋势和可能性。

# 本书使用的惯例

本书中使用以下排版惯例：

*斜体*

表示新术语、URL、电子邮件地址、文件名和文件扩展名。

`等宽`

用于程序清单，以及在段落内引用程序元素，如变量或函数名称、数据库、数据类型、环境变量、语句和关键字。

**`等宽粗体`**

显示用户应该直接键入的命令或其他文本。

###### 提示

此元素表示提示或建议。

###### 注意

此元素表示一般注意事项。

# 致谢

## 来自 Sandra

我要感谢 Rebecca Novak，她为我们提供了撰写本书的独特机会，以及我的合著者 Shubham，他邀请我与他合作，并在整个过程中始终是一个极具支持和积极性的合作伙伴。

我们的书如果没有我们出色的编辑 Sarah Grey，就不会成为今天的样子，她总是督促我们对读者更具移情力。我还要向我们的技术编辑 Daniel Ibáñez 和 Matteus Tanha 表示深深的感谢，他们帮助我们使书籍在概念上更加坚实，还要感谢 Vladimir Alexeev 和 Natalie Pistunovich，他们为我们提供了很好的技术编辑建议。

感谢在 GPT-3 社区内同意与我们分享他们的经历，并帮助塑造第四章和第五章，并教育我们关于 GPT-3 产品生态系统的以下组织和个人：OpenAI 的 Peter Welinder，Microsoft Azure 的 Dominic Divakaruni 和 Chris Hoder，Algolia 的 Dustin Coates 和 Claire Helme-Guizon，Wing VC 的 Clair Byrd，Viable 的 Daniel Erickson，Fable Studio 的 Frank Carey 和 Edward Saatchi，Stenography 的 Bram Adams，Quickchat 的 Piotr Grudzień，Copysmith 的 Anna Wang 和 Shegun Otulana，AI2SQL 的 Mustafa Ergisi，Bubble 的 Joshua Haas，GitHub 的 Jennie Chow 和 Oege de Moor，以及 Bakz Awan 和 Yannick Kilcher。

我也想感谢我的母亲 Teresa，我的姐姐 Paulina，我的爷爷 Tadeusz，我的表姐 Martyna，以及在我忙于写作时陪伴我的朋友和同事。

## 来自 Shubham

这本书是 Rebecca Novack 找到我的博客并邀请我讨论在大型语言模型领域写一本独特的书的结果。接下来，我要感谢我的合作者 Sandra，她像一个完美的伙伴一样填补了空白并补充了我的技能。尽管在写这本书时我们面临了许多挑战，但由于 Sandra 能够将即使是最紧张的情况转变为有趣的情景，我们还是玩得很开心。

我很感激能与像 Sarah Grey 这样优秀的编辑一起合作。她在塑造这本书的最终形式上做得很好。编辑后，这本书就像是活过来了一样。还要特别感谢 Nicole Butterfield 在 Rebecca 在书的制作过程中不得不离开后承担责任。

我们的技术编辑 Daniel Ibáñez 和 Matteus Tanha 在给我们关于何时该去何时该走的极好反馈上发挥了至关重要的作用。非常感谢 OpenAI 团队，特别是 Peter Welinder 和 Fraser Kelton，他们在整个旅程中始终是支持和指导的不竭源泉。我还要感谢我们采访过的所有创始人和行业领袖，感谢他们宝贵的时间和宝贵的见解。

感谢我的妈妈 Gayatri，我的爸爸 Suresh，我的哥哥 Saransh，以及在写作过程中一直支持我的所有朋友和同事。另外，还要感谢 Plaksha 大学的教师和创始人们，他们给了我超越常规思维、挑战现状的机会。我在 Plaksha 的 Tech Leaders 计划中的教育和经验使我能够高效地完成这本书。