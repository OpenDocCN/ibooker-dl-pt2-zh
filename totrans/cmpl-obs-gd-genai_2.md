# 2 管理生成型 AI

### 本章内容包括

+   掌握如何以最高效的方式访问和使用 AI 模型进行交互

+   配置模型以尽可能地满足你的具体需求

+   利用 OpenAI Playground 来更好地了解控制 AI 的关键工具

把巧妙的提示投给一个 AI 聊天界面肯定会产生令人印象深刻的结果。但是如果忽视模型配置中的细节，你就会错过大部分 AI 的潜在价值。所以在本章中，我们将开始找出应该转动哪些旋钮以及转动到什么程度的过程。（以及你绝对应该避免的哪个大红按钮！）

当然，我不知道，等你读到这里，整个过程可能已经自动化了。你键盘上轻轻闪烁的蓝色光？那将是 GPT 现在用来直接下载你最内心的目标和欲望的脑波扫描仪。

你的结果现在可以使用了。

## 2.1 访问 GPT 模型

如果你还没有这个荣幸，大多数流行的交互式 AI 平台在你尝试它们之前都需要你创建一个帐户。对于 OpenAI 的 ChatGPT，你可以在 chat.openai.com/auth/login 进行注册。即使你被要求提供信用卡信息，你在实际上被收费之前会有足够的警告。只要别忽略了这些警告。

一旦你注册成功，ChatGPT 的界面在这里。

现在怎么办？

除了 ChatGPT，你不需要拥有电气工程博士学位就可以意识到，微软的必应搜索引擎让你可以在 Edge 浏览器内访问 GPT-4。我想在这里也提一下谷歌的 GPT 竞争对手 Bard，但是我在加拿大。Bard 在这里还没有出现。事实上，你会发现在不同的地理、商业或者技术上，对于访问不同的 AI 服务会有各种各样的限制。要耐心和灵活。

除了那些由它们的创建者直接提供的网络服务，还有很多第三方网络项目，比如 ChatPDF（用于分析 PDF 文档）和 Rytr（用于生成写作内容），它们提供了优秀的托管应用程序，适用于各种特殊用例。对于使用这些工具来说，并没有什么特别复杂的。我们以后会更详细地讨论这些服务。

但是那些都是消费级的东西。没关系。但是你可能会说，严肃的工作是在“校外”发生的。也就是说，高生产力的交互，比如仔细配置你的模型，让你的 AI 在大量的*自己的*数据中自由运行，或者自动化多轮的提示和完成，并将回答融入到你的代码驱动工作流程中。

无论你使用的是哪种模型，*这*种访问都将通过应用程序编程接口（API）进行。如下图所示，API 充当软件应用程序之间的桥梁，允许它们进行通信和交互。它定义了一组规则和协议，允许一个应用程序向另一个应用程序请求服务或数据。API 提供给具有适当授权的开发人员访问服务的特定功能。它们通过指定请求应如何结构化以及响应将如何格式化来实现无缝集成。

##### 图 2.1 典型的 API 架构

![gai 2 1](https://drek4537l1klr.cloudfront.net/clinton6/v-3/Figures/gai-2-1.png)

本书后面你将看到的很多技术示例将通过 API 实现。出于实际原因，这些示例大多将使用 OpenAI 的模型和基础设施。但是广义的基础方法应该也大多适用于其他服务（一旦它们变得广泛可用）。

所以编写自己的 AI 的道路通过 API。但是如果你以前从未做过这种事情，不用担心。我会为你提供所有背景和技术细节，以确保一切都能正常运行。

在我们*进入*那里之前，我们应该先查看 OpenAI 的 Playground。

## 2.2 通过“游戏”学习

Playground，如下图所示，甚至在 ChatGPT 之前就已经存在了，那是我第一次与 GPT 进行互动的地方。尽管要记住，与 AI 世界中的其他一切一样，界面可能在你使用之前至少会变化两次。我们将在本章中使用 Playground 来学习如何与 GPT 互动。

##### 图 2.2 OpenAI 的 Playground 界面

![gai 2 2](https://drek4537l1klr.cloudfront.net/clinton6/v-3/Figures/gai-2-2.png)

你可以通过你的 OpenAI 登录账户进入 Playground。与之前的持续对话不同，后续交互不会受到先前提示和完成的影响，Playground 中的默认文本字段一次只提供一个交换。其基于的模型可能也比 ChatGPT 版本要旧一些，也不太精细。

但是有两个方面使得 Playground 与 ChatGPT 不同。一个是屏幕右侧显示的配置控件，如上图所示，第二个是右上角的*查看代码*功能。正是这些功能使 Playground 主要成为一个教育工具，而不仅仅是另一个 GPT 接口。

## 2.3 获取 Python 代码示例

我们将在本章的下一部分逐个查看这些功能。但是，使用代码访问 GPT API 可能会在长期内为您提供最大的价值，我真的想立即向您展示*查看代码*的功能是什么。下面的图像显示了一个典型的 Playground 会话，我在其中键入了提示，然后点击了“查看代码”按钮，选择了“Python”选项。我看到的是可工作的代码，假设您在第 4 行添加了有效的 OpenAI API 密钥，可以从任何连接到互联网的计算机上复制并运行。

##### 图 2.3 Playground 的查看代码工具显示的 Python 代码

![gai 2 3](https://drek4537l1klr.cloudfront.net/clinton6/v-3/Figures/gai-2-3.png)

现在不要担心细节，但请花点时间浏览包含在`openai.Completion.create()`方法中的参数。右侧游乐场中当前选择的模型在“模型”字段中（`text-davinci-003`），“Explain the purpose of…​”实际提示也在其中。事实上，我选择的每个配置选项都在其中。换句话说，我可以在游乐场中尝试任何组合的配置，然后复制代码并在任何地方运行它 - 或其变体。

事实上，这正是您学习如何使用 API 的地方。

## 2.4 访问 CURL 代码示例

下一个图像向我们展示了如果我决定使用命令行工具 curl 而不是 Python，那么完全相同的提示会如何工作。除了 Python 和 curl，您还可以在 node.js 和 JSON 中显示代码。

##### 图 2.4 Playground 的查看代码工具显示的 curl 代码

![gai 2 4](https://drek4537l1klr.cloudfront.net/clinton6/v-3/Figures/gai-2-4.png)

`curl`是一个备受尊敬的开源命令行工具，通常默认可用。要确认它在您的系统上可用，请简单地在任何命令行提示符下键入`curl`。您应该会看到一些帮助消息，其中包含了正确使用的建议。

还有一件事。下表显示了每个可用的 OpenAI 模型以及它们关联的 API 终端点。端点是您在代码中可以使用的地址，用于访问资源。除了具有这些信息的价值之外，这也很重要，因为它向我们展示了您可以发送的*种类*提示。除了您预期的 `completions` 操作之外，还有 `edits`、`transcriptions`、`translations`、`fine-tunes`、`embeddings` 和 `moderations`。我们将在本书后面更多地讨论如何使用它们。但请记住所有这些。

| 终端点 | 模型名称 |
| --- | --- |
| /v1/chat/completions | gpt-4, gpt-4-0314, gpt-4-32k, gpt-4-32k-0314, gpt-3.5-turbo, gpt-3.5-turbo-0301 |
| /v1/completions | text-davinci-003, text-davinci-002, text-curie-001, text-babbage-001, text-ada-001 |
| /v1/edits | text-davinci-edit-001, code-davinci-edit-001 |
| /v1/audio/transcriptions | whisper-1 |
| /v1/audio/translations | whisper-1 |
| /v1/fine-tunes | davinci, curie, babbage, ada |
| /v1/embeddings | text-embedding-ada-002, text-search-ada-doc-001 |
| /v1/moderations | text-moderation-stable, text-moderation-latest |

##### 要点

无论你使用哪种 AI，确保你了解所有可用选项，这样你就可以优化你的环境。

## 2.5 完成配置

你可以把“完成配置”看作是一种微调，这样说也不算错。但是，在 AI 的背景下，“微调”这个术语可能有更具体的含义。我们将在第六章和第九章花更多时间讨论这个话题。

在我开始解释每个配置的工作方式之前，这是一张图片，应该可以帮助你想象 AI 模型在生成响应之前对你的提示做些什么。

##### 图 2.5：参数如何应用于 AI 提示

![图 2.5](https://drek4537l1klr.cloudfront.net/clinton6/v-3/Figures/gai-2-5.png)

正如你所见，一个典型的语言模型可能会立即产生一个初步的草案响应（图中的“生成输出”）。但是，在与你分享之前（“返回输出”），它将首先测试其是否符合你可能设置的任何偏好（即，温度、频率等）。我们很快就会看到这些偏好起作用 - 它们可以控制提示的语调、创造性、焦点、冗长甚至成本。

现在看看游乐场中的这些控件是什么样子的。

##### 图 2.6：游乐场 UI 中的工具上半部分选择

![图 2.6](https://drek4537l1klr.cloudfront.net/clinton6/v-3/Figures/gai-2-6.png)

现在让我们看看这些到底是什么。为了让你保持方向，我们将涵盖每个配置类别：

+   模式

+   温度

+   最高 P 值

+   停止序列

+   频率惩罚

+   存在惩罚

+   最佳选择

+   注入起始文本

为了让你有些背景，想象一下你正在构建一个 Web 应用程序，为用户提供关于你的酒店的问题的即时响应。你可能最初会要求用户从一系列类别中进行选择（“餐饮和娱乐”，“旅行规划”等）。根据他们选择的类别，你希望微调你的聊天工具，以便响应与用户的期望相匹配。

这些配置可以帮助你创建这样的定制。

### 2.5.1 设置模式

根据你使用的模型不同，**模式**下拉菜单可能有三个选项：聊天、完成和编辑。完成和聊天提供了我们已经习惯的熟悉的完成和聊天体验。如果你有一些文本想要以某种方式重新处理，你可以选择编辑模式，在输入部分输入你的文本，并在下面的说明字段中输入你想要更改的文本。游乐场建议“修复语法”作为可能的指令，但你可以自由使用你自己的指令。我们将在下一章中了解更多关于这种操作的信息。

**模型**下拉菜单中预置的列表显示了当前选定模式下可用的所有 OpenAI 模型。此列表将根据您选择的模式动态变化。显然，您会想要选择一个最适合您的需求和预算的模型（如上所述）。

### 2.5.2 设置温度

**温度**控制生成输出时所使用的随机性程度。它允许用户调整输出中的创造性和不可预测性水平。通过将温度设置为介于`0`和`2`之间的值（默认为`1`），AI 可以生成不同类型的输出，从高度创造性和不可预测性（即 2）到高度结构化和保守性（即`0`）。

让我们考虑一个使用聊天机器人场景的例子，其中用户询问餐厅推荐：

##### 提示

用户：“你能推荐附近的好餐厅吗？”

我们可以使用不同的温度设置来生成具有不同随机性程度的响应。更高的温度（例如 1.3）鼓励语言模型生成更多样化和创造性的响应，即使它们可能不太集中或准确：

##### 响应

温度 1.3：助手：“当然！试试角落里那家舒适的小咖啡馆怎么样？他们供应美味的食物，从美味的汉堡到异国情调的寿司。那里的用餐体验绝对让你大开眼界！”

在这种情况下，高温设置导致了一个更有想象力的回应，提出了各种食品选择，并强调了“冒险的用餐体验”。

另一方面，较低的温度（例如 0.2）鼓励语言模型生成更确定性和集中的回应，通常固守安全和传统的选择：

##### 响应

温度 0.2：助手：“当然！我建议你去主街上的意大利餐厅。那里有正宗的意大利面和令人垂涎的披萨。你绝对不会失望！”

通过降低温度，回应更为直接，并专注于特定的烹饪风格和场所，提供了一个安全可靠的建议。

### 2.5.3 设置 Top P 值

**Top P**（也称为核采样或“无惩罚采样”）是帮助控制生成文本多样性的参数。它涉及在序列中选择下一个标记的最有可能的单词，考虑累积概率阈值（P）。它不是从整个词汇表中生成，而是将选择范围缩小到那些累积概率超过 P 的最有可能的单词的子集。这有助于控制输出的长度和多样性，同时保持连贯性。

使用 Top P 抽样方法时，模型根据概率阈值（p）选择最有可能的下一个词，这允许更多样化和受控制的输出。累积概率超过阈值的单词将被考虑，确保在生成的文本中平衡可预测性和创造性。简单来说，“top p”允许模型超越明显的选择，同时保持连贯性。这就像给 AI 一点自由来给你带来惊喜，同时确保生成的文本仍然有意义。当您需要创意回复而不完全偏离主题时，这种技术特别有用。

通过调整 Top P 值，用户可以影响模型响应中的随机性或多样性。较高的值（例如，`0.9`）包括更大的潜在标记集，使输出更加多样化，而较低的值（例如，`0.1`）限制了选择，导致更加聚焦和确定性的输出。默认的 Top P 值为`1`。

这是一个用户询问天气信息的例子：

##### 提示

用户：“今天的天气怎么样？”

我们可以探索不同的 Top P 值对响应生成的影响。

##### 响应

Top P 0.2（高度聚焦）：助手：“今天的天气是晴朗的，最高气温为摄氏 25 度。是享受户外活动的完美天气。”

使用较低的 Top P 值，模型仅选择最可能的下一个词，导致聚焦和确定性的响应，通常更可靠但变化较小。

##### 响应

Top P 0.8（更多样化）：助手：“今天的天气晴朗、温暖、令人愉快。你可能想戴上太阳镜，出去享受充满乐趣的一天！”

使用较高的 Top P 值，模型会考虑更广泛范围的可能的下一个词，从而产生更多样化的响应。这可以在生成的文本中引入变化，提供表达相同信息的不同方式。

尽管 Top P 和 Temperature 看起来相似，但 Temperature 控制语言生成中的随机性：较高的值（例如，1.0）增加多样性，较低的值（例如，0.2）产生更可预测的输出。相反，Top-p 抽样设置概率阈值（p）以从最有可能的词组中进行选择，根据阈值（例如，p=0.9 用于更多多样性，p=0.2 用于较少多样性）调整输出的多样性。

一般情况下，可以更改 Temperature *或* Top P，但不能同时更改两者。

### 2.5.4 使用停止序列

**停止序列**是用于指示生成的响应结束或提示模型停止生成进一步文本的特殊标记。这些标记通常添加到输入提示中以控制生成的输出长度。

在英语中，常见的句末标记示例是句号（.），后跟一个空格。在编程语言中，常见的停止序列可能是一对花括号（"{}"）来表示代码块的结尾。在 HTML 或 XML 中，像 "</tag>" 这样的闭合标签表示元素的结束。

需要注意的是，像 GPT 这样的现代语言模型不一定依赖于显式的停止序列来生成文本。相反，它们通常使用诸如标记化和上下文窗口之类的技术来理解何时自然结束句子或段落。此外，它们可能在内部使用特殊标记，如 "<eos>"（序列结束），但这些细节通常对用户进行了抽象处理。

例如，在解释课程的中途，可以配置虚拟讲师说，“我们今天就到这里吧。请给我复述一下这节课的三个主要观点。” 学生回答了三个主要观点（符合所需的停止序列）后，讲师可以说，“是的，很棒！好了，今天的课到此结束。”

### 2.5.5 设置频率惩罚

**频率惩罚** 用于阻止重复或冗余的输出。它有助于解决模型倾向于产生重复或过长短语的常见问题，导致响应不够连贯和多样化。通过应用频率惩罚，用户可以控制生成多样化响应和避免重复模式之间的权衡。

惩罚是根据已在输出中出现的生成标记或标记序列的次数计算的。当应用惩罚时，模型对标记的概率分布进行调整，以减少生成已使用标记的可能性。频率惩罚的目的是鼓励模型探索替代选项并生成更多样化和连贯的响应。

惩罚值（可以介于 `-2.0` 和 `2.0` 之间）可以根据所需的重复避免级别进行调整。较高的惩罚值导致更强烈地避免重复，而较低的值允许生成的输出具有更多的灵活性。找到正确的平衡很重要，以确保生成的文本保持连贯性和上下文相关性，同时避免过多的重复。

考虑一个用户要求为新智能手机提供一些想法的示例：

##### 提示和响应

用户：为新智能手机提供一些想法。

模型：当然！以下是一些想法：高分辨率显示屏、多个摄像头镜头、快速处理速度、长续航时间和时尚设计。

那个语言模型生成的想法已经很常见了 - 它几乎没有突破性。然而，如果你加上一个频率惩罚：

##### 提示和响应

用户：在使用频率惩罚的情况下，为新智能手机提供一些独特和罕见功能的想法。

模型：当然！如何把智能手机和全息显示器结合起来，以投射 3D 图像，采用石墨烯电池实现即时充电，设计可定制的模块化结构，使用户可以更换硬件组件，内置 AI 语言翻译器实现实时对话，以及读取用户手掌上独特静脉纹理的生物识别系统？

在这种情况下，通过使用频率惩罚，模型更有可能生成涉及不太常见的单词或概念的想法。这导致了更具创新性和想象力的建议，符合您提出独特产品特性的目标。

### 2.5.6 设置存在惩罚

**存在惩罚** 是 GPT 模型中的一个参数，有助于控制生成文本中短语和单词的重复。它旨在防止模型在生成的输出中过于频繁地重复相同的短语或单词。存在惩罚修改概率分布，以减少输入提示或种子文本中存在的单词。这鼓励模型生成未明确存在于输入中的单词和涉及的主题。

尽管`存在`和`频率`惩罚似乎有重叠之处，但它们并不相同。频率惩罚是与特定标记已被采样的频率成比例的贡献。它阻止模型在生成文本中过于频繁地重复相同的单词或短语。另一方面，存在惩罚是一次性的、增加的贡献，适用于至少被采样一次的所有标记。它修改概率分布，以减少输入提示或种子文本中存在的单词。这鼓励模型生成未在输入中的单词。

我们可以探索不同存在惩罚值对响应生成的影响，同时与频率惩罚进行比较。想象一下，您提示模型：“告诉我关于我最喜欢的体育队最近的表现。”

##### 回应

存在惩罚 0.2（减少规避）：

助手：“您最喜欢的体育队在最近的比赛中表现异常出色。他们展示了卓越的团队合作和战略性的比赛，取得了几场胜利。”

采用较低的存在惩罚，模型可能更频繁地生成包含所需关键词或概念的响应，因为它不太倾向于避免使用它们。而使用频率惩罚进行相同操作，结果会是：

##### 回应

频率惩罚 0.2（减少重复）：

助手：“您最喜欢的体育队最近表现出色。他们展示了出色的技巧、协调能力和改变比赛局势的策略，取得了一系列的成功。”

与存在惩罚相比，频率惩罚侧重于减少特定短语或响应的重复，而不考虑它们与用户输入的相关性。

通过调整存在惩罚，您可以控制 AI 在生成的文本中遵循特定关键字或概念的程度。较低的值可能导致模型更频繁地提到所需的主题，而较高的值则鼓励模型避免过多地重复这些主题。

下面是如何在语言模型提示中使用高存在惩罚的示例。想象一下，您正在使用语言模型来生成一个故事或对话，并且希望确保生成的文本避免提及任何暴力或图形内容。您希望应用高存在惩罚来确保模型严格避免使用与暴力相关的单词或短语。

##### 提示

用户：创建一个关于两位冒险家为了拯救他们的王国免受巨大威胁的故事。应用高存在惩罚，避免描述任何暴力或图形场景。

通过使用高存在惩罚，您可以引导语言模型生成符合特定内容指南的响应，使其适用于各种需要避免某些主题或语言的情境。

除了您在游乐场页面上可以看到的配置控件之外，还有一些其他控件既常见又有用：

### 2.5.7 使用“最佳选择”

当从生成式 AI 模型生成响应时，有时可能会收到多个候选输出。**最佳选择**方法涉及根据某些标准从这些候选项中选择最合适或最高质量的响应。默认设置（`1`）将流式传输所有输出而不进行任何选择或过滤。较高的值（最高可达`20`）将增加您所看到的可能性生成与输出之间的比率。

“最佳选择”方法的目的是通过手工选择最有利的响应来策划和完善输出中的内容。它使您能够更多地控制最终输出，确保它符合您的期望标准或与生成式 AI 模型的预期目的相一致。但请记住：最佳选择值越高，您为每个输出支付的费用就越多。

例如，在文本摘要任务中，您可能希望识别出捕捉文档或文章精华的最重要的短语或句子。您可以使用“最佳选择”来提取基于其重要性或相关性的前 n 个短语或句子，然后使用这些短语来生成原始文本的摘要。

### 2.5.8 使用注入起始文本设置

“注入开始文本”或“输入前缀”是指根据用户提供的特定初始文本来指导或约束模型的输出。它涉及在输入序列开头处事先添加或插入提示、问题或上下文，以影响生成的回复。通过注入开始文本，您可以为模型提供额外的上下文或信息，以帮助其将输出引导到所需的方向。与我们之前看到的其他提示工具不同，注入的开始文本成为输入提示本身的一部分，并用作生成的回复的开头。这在您想要生成的文本更加专注、具体或适用于特定上下文的情况下非常有用。

例如，如果您正在使用语言模型在客户支持聊天机器人中生成回复，可以在模型生成回复之前插入“用户：您的产品的退货政策是什么？”等开始文本。这有助于给对话框架并确保模型理解用户查询的上下文。

与指定文本前缀完成不同，“注入重新启动文本”允许用户在一个完成中插入文本，以“继续”某种模式化的对话结构。

想必你可以想象，在 API 的帮助下，GPT 还有很多酷炫和精彩的用途。在本书的剩余部分中，我们肯定会触及其中的许多方面。但是你可以（而且应该）经常去 API 参考页面查看。

##### 要点

除了简单的信息获取请求之外，任何比较复杂的生成型 AI 操作（特别是以程序化方式交付的自动提示）都可以通过调整模型参数来更有效地执行。所以考虑超越默认设置，比如频率和温度等内容。

## 2.6 小结

+   生成型 AI 模型有多个类别，包括像 GPT 和 PaLM-2 这样的软件框架，以及像 GPT 的 davinci 和 ada 这样更具体的基于任务的模块。每种模型都有其最佳应用场景。

+   OpenAI 的 Playground 是一个有价值的工具，可用于了解 GPT 提供的配置选项并生成用于通过 OpenAI API 运行提示的代码。您应该将 Playground 作为自定义构建代码的来源，以执行通过 OpenAI API 的提示。

+   温度、存在惩罚和最优选择等配置控制变量可以用于微调模型提示。无论使用哪个 AI 模型，通常都有互动工具可用于应用这些控制变量。

+   OpenAI API 参考指南是一个重要的资源，把它当做你最好的朋友。

+   我们探索了微调在更大上下文中的应用，从中快速了解到了 LLM 所具备的一些灵活性。