# 第四章：GPT-3 作为下一代创业公司的发射台

在发布 GPT-3 之前，大多数人与人工智能的互动局限于某些特定任务，比如要求 Alexa 播放你喜欢的歌曲或使用 Google 翻译与不同语言交流。研究人员已成功开发出能够执行日常任务的人工智能，但到目前为止，人工智能尚未能够像人类一样在没有清晰、明确定义的指令的情况下发挥抽象任务方面的创造潜力。

随着 LLM 时代即将来临，我们正在目睹一个重大的范式转变。LLM 向我们展示了，通过增加模型的规模，它们可以执行类似于人类的创造性和复杂的任务。现在最大的问题是：人工智能能够执行创造性活动吗？

人工智能的创造潜力一直是一个令人兴奋的研究领域，尽管大部分隐藏在像 Google 和 Facebook 这样的公司的紧密研发墙后。GPT-3 正在改变我们与人工智能的互动方式，并赋予人们建立下一代应用的能力，这些应用在其发布之前似乎是一个遥不可及的想法。IBM 研究的多媒体和视觉经理约翰·史密斯指出：“对于人工智能来说，随机提出新颖的东西很容易。但要提出新颖、意外且有用的东西却很难。”而 Somatic 的 CEO 杰森·托伊则问道：“我们能否将人类认为美丽和富有创意的东西放入算法中？”^(1)

# 作为一种服务的模型

在本章中，我们将向您展示 GPT-3 如何通过为创意企业家提供正确的技术，激发他们的想象力，推动下一波创业浪潮。我们还将探讨人工智能研究在多个领域的商业化进展。我们将与支持这些倡议的风险投资家之一交谈，以了解蓬勃发展的 GPT-3 经济的财务方面。

OpenAI API 的创建故事与本章中许多创业公司的故事类似。我们采访了 OpenAI 的彼得·韦林德。他告诉我们的是一个大胆实验、快速迭代和利用智能设计实现规模经济的故事（以尽可能低的成本为条件提供大规模的强大模型）。

Welinder 概括了 OpenAI 的使命，提出了三个关键点：“开发通用人工智能，确保其安全，然后最后将其部署到世界上，以使其最大程度地造福所有人类。”因此，公司正在致力于开发可以应用于越来越广泛需求的人工智能。

希望尽快且安全地实现通用人工智能，OpenAI 决定押宝的技术之一是大型语言模型，具体是 GPT-3。Welinder 提到尝试 GPT-3 时说：“这是我们第一次感觉到，‘实际上，这似乎相当有用，它在许多学术基准任务上取得了最先进的结果等等。’”

对于可能性感到兴奋的 Welinder 和四位同事进行了讨论，讨论如何最好地利用这个算法：建立一个翻译引擎？一个写作助手？一个客户服务应用？然后 Welinder 说，“为什么不直接将这项技术提供为 API，让任何开发人员在其基础上构建自己的业务呢？”

API 的方法与 OpenAI 的目标和使命相一致，最大程度地促进了技术的采用和影响，赋予社区成员发明应用程序的能力，这些应用程序 OpenAI 团队无法预测。这也使产品开发交给了全球技术开发人员，释放出 OpenAI 团队专注于其真正擅长的事情：开发健壮、开创性的模型。

到目前为止，研究人员一直专注于设计可扩展、高效的训练系统，以充分利用 GPU 的效率。但是很少关注在实际数据上运行这些模型并为实际应用得到一些结果。因此，OpenAI 团队决定加倍努力提升核心 API 体验，专注于快速推理和低延迟等方面。

在计划推出 API beta 版的六个月前，据 Welinder 称，研究人员将延迟时间减少了约十倍，同时将吞吐量增加了数百倍：“我们投入了大量工程工作，确保这些模型的 GPU 尽可能高效，以及以非常低的延迟调用它们，并使其可扩展。”通过 API 使用模型而不需要自己的 GPU，使其成本效益高，并且对普通开发人员来说易于访问，可以尝试各种用例和尝试新事物。非常低的延迟也很重要，以便轻松进行迭代。“你不想投入某些东西，然后等待几分钟才能得到响应，这在 API 的最早阶段是这样的情况。而现在，你可以实时看到模型输出的内容，”Welinder 说。

OpenAI 认为模型会不断增长，这会使开发者难以部署它们；团队希望消除这一障碍。“因为你需要如此多的 GPU 和 CPU 来应对一个使用案例，这样做会花费你太多成本。你自己部署这个模型是没有经济意义的，” Welinder 说道。相反，公司决定通过 API 与开发者分享模型。“成千上万的开发者使用相同的模型，这就是你可以实现规模经济的方式，” Welinder 补充道。“这降低了每个人访问这些模型的价格，并进一步扩大了分发范围，让更多人可以尝试这些模型。”

将 OpenAI API 私人测试版发布带来了很多惊喜。之前备受关注的模型 GPT-2 很少有真实世界的应用案例，所以团队希望 GPT-3 能够更有用。事实证明确实如此，并且非常迅速。

另一个惊喜，Welinder 说，“我们平台上很多人不是程序员。他们是各种类型的作者、创作者，是设计师和产品经理等。”在某种程度上，GPT-3 改变了成为开发者的意义：突然之间，建立人工智能应用程序，你不需要知道如何编程。你只需要擅长使用提示来描述你想让人工智能做什么（如第二章中所讨论的）。

Welinder 和他的团队发现，“很多擅长的人根本没有机器学习背景”，而那些有机器学习背景的人则必须放弃以往对许多问题的思考方式才能使用 GPT-3。许多用户构建了基于 GPT-3 的应用程序而不需要编码。OpenAI 团队，无意中，降低了创建应用程序的障碍：这是迈向普及人工智能的第一步。“核心战略是使 API 对尽可能多的人可用，”Welinder 说：“确保使用我们的技术的门槛低是我们使命的核心。这就是我们建立这个 API 的原因。” GPT-3 的另一个意外用途是编码。模型的编码潜力的早期迹象促使 OpenAI 加倍努力设计编码用例。他们的努力导致了 Codex，在 2021 年中期发布。^(2)

除了惊人多样的用例，API 还孕育了一个全新的创业生态系统：“在发布 API 几个月后，就有几家公司完全建立在 OpenAI API 之上。其中许多公司现在已经以相当高的估值融资，”Welinder 表示。

OpenAI 的核心原则之一是与客户密切合作。Welinder 表示：“每当我们有新的产品功能时，我们都会尝试找到我们知道会发现这些功能有用的客户，并创建直接的沟通渠道，在那里我们提供他们早期访问权限。”例如，在更广泛地在 API 中发布该功能之前，OpenAI 与几个客户合作对搜索功能进行了优化。

OpenAI 主要关注确保 AI 的安全和负责任使用。除了许多积极的结果外，随着 AI 变得更加普及，公司也看到了滥用的潜力不断增长。他们选择在私人测试版中推出 API 的主要原因之一是了解人们如何使用模型并检查其滥用的潜力。他们尽可能多地检查不良模型行为的实例，并利用所学知识来指导他们的研究和模型训练。

Welinder 从 API 驱动的项目的广度和创造力中获得了灵感。“未来十年将是令人兴奋的，因为人们将在这项技术基础上构建的所有东西。我认为通过共同努力，我们可以创建一些真正良好的防范措施，以确保这些技术、这些即将构建的应用对我们的社会将会非常非常积极。”

# 新创业生态系统：案例研究

在 OpenAI 发布 API 不久之后，初创公司的景观充满了使用它来解决问题的公司。这些企业家是最先进的自然语言处理产品的先驱，并且他们的经历对于计划基于 OpenAI API 的未来商业应用的人尤为有启发性。本章的其余部分通过对一些以 GPT-3 为核心的顶尖初创公司领导人的采访，展示了这个充满活力的景观。他们与我们分享了他们迄今在创造性艺术、数据分析、聊天机器人、文案撰写和开发者工具等领域所学到的知识。

## GPT-3 的创造性应用：Fable Studio

GPT-3 最令人兴奋的能力之一是讲故事。您可以给模型一个主题，并要求它在零-shot 情境下撰写故事。

这些可能性使作家们扩展了他们的想象力，并产生了非凡的作品。例如，由 Jennifer Tang 执导并与 Chinonyerem Odimba 和 Nina Segal 共同开发的戏剧 [*AI*](https://oreil.ly/XJENe)，描绘了人类与计算机思维之间独特的合作关系，借助 GPT-3 的帮助。作家 K Allado-McDowell 将 GPT-3 视为与其共同撰写书籍 [*Pharmako-AI* (Ignota Books)](https://oreil.ly/uemTP) 的合作者，Allado-McDowell 表示，“重新构想了面临多重危机的世界的控制论，对我们如何看待自己、自然和 21 世纪的技术产生了深远的影响。”

我们与 Fable Studio 联合创始人兼首席执行官 Edward Saatchi，以及 Fable Studio 首席技术官 Frank Carey 坐下来，了解他们在使用 GPT-3 创造新型互动故事类型的过程。Fable 将 Neil Gaiman 和 Dave McKean 的儿童书 *The Wolves in the Walls* 改编成了一部获得艾美奖的虚拟现实（VR）电影体验。Lucy，电影的主角，可以通过 GPT-3 生成的对话与人进行自然交流。Lucy 甚至于 2021 年亮相于圣丹斯电影节。

Saatchi 和 Carey 注意到他们的观众正在与露西建立情感联系。这促使他们专注于使用 AI 创建虚拟存在，以及一种将 AI 和叙事编织在一起的新类型的叙事和娱乐。正如 YouTuber Bakz Awan 所说，“我们将拥有全新类型的电影和体裁：我们将拥有交互式、综合体验。”

Carey 解释说，观众通常认为 AI 承担了角色的角色，就像演员一样：一个 AI 对应一个角色。相反，Fable 的 AI 是一个讲故事者，它拥有各种各样的角色。Carey 相信可以开发出一个与最优秀的人类作家一样熟练和有创造力的 AI 讲故事者。

虽然露西的对话大多是通过文字和视频聊天进行的，但 Fable 还在尝试将 GPT-3 应用于 3D 模拟世界，以获得沉浸式虚拟现实体验。团队使用 AI 生成音频和手势，并同步唇语动作。他们使用 GPT-3 生成了角色与观众互动的大部分内容。其中一些内容可以预先撰写，但大部分必须即兴创作。露西的合作者们广泛使用了 GPT-3，在她的圣丹斯出现期间以及在电影创作过程中都是如此。露西还出现在 Twitch（一种交互式直播平台，[她似乎在播放游戏或讲故事](https://oreil.ly/sQIiX)）。在这两种情况下，Carey 说，“超过 80%的内容是使用 GPT-3 生成的。”

这与团队早期的纯文本实验形成了鲜明对比，这些实验在很大程度上是由人为撰写的，并且遵循了更线性的叙事。Fable Studio 团队通常不会使用 GPT-3 实时处理观众的不可预测的回应；他们处理这些的技术早于 GPT-3。但是，他们有时会将 GPT-3 用作写作伙伴或观众的替代者，以考虑观众可能给出的潜在回应。

Carey 解释道，GPT-3 对于人类作者来说也是一个有用的工具：“对于即兴内容，我们正在使用 GPT-3 进行测试，这样你就可以将 GPT 视为人类，你就像在扮演角色一样。与 GPT-3 来回交流有助于你想出，比如说，在这种情况下，某人会问什么？接下来会有什么？这有助于作者尽可能多地涵盖对话的结果。”这有助于作者涵盖尽可能多的对话结果。“有时它曾是一个写作伙伴，有时它是一些能填补正在发生的事情周围空白的东西，”Saatchi 说。“所以我们可能会想：这个角色这周会发生什么？下周这个角色会发生什么？GPT-3 [填补了]其中一些空白。”

Fable 团队在 2021 年圣丹斯电影节上充分利用了 GPT-3 的实验，在那里 Lucy 与节日参与者实时合作创作了她自己的短片 *德古拉：血色冷汤*[³]，而 Fable Studio 和参与者则在策划她产生的想法，与参与者交流，并将观众的想法反馈到 GPT-3 中。

用 GPT-3 给一个一致的角色赋能是一个特殊的挑战。Saatchi 解释说，GPT-3 非常适用于从角色转向参与者的用例，比如疗法会话，以及对于那些对它们有“非常丰富的关于它们的知识库，比如名人或者像耶稣、圣诞老人或者德古拉这样的原型角色。但显然，它的使用范围会受到已经写入的信息的限制，”他指出，任何与使用 GPT-3 动力驱动角色进行广泛互动的人很快就会达到 GPT-3 的限制。“它试图给你提出的故事找到一个好的答案。但如果你在提示中讲述一个荒诞的故事，它也会提出荒诞的答案。对吧？所以它不是一个讲真话的人。我会说它天生就是一个讲故事的人；它只是试图在语言中找到模式。”关于 GPT-3，许多人没有意识到的一点是，它的底线任务是讲故事，而不是“真相”，Carey 说。

“仅仅使用 GPT-3 生成一堆随机情景是一回事，但确保它是以那个角色的语调发言是另一回事，” Carey 补充道。“因此，我们有一些技巧用来创建那些提示，以便角色对 GPT-3 有明确的定义。” 他承认团队在确保 GPT-3 理解角色的语音并保持在角色可能的回应范围内方面付出了额外的努力。他们还必须避免让参与者影响角色，因为 GPT-3 可以捕捉到微妙的信号。Carey 解释说，如果 Lucy 与成年人互动，“它只会配合气氛，但如果 Lucy 是一个八岁的孩子，它可能会从参与者那里捕捉到更多的成年人气息，并将其反馈给他们。但我们实际上希望 [Lucy] 以八岁孩子般的语气说话。”

说服 OpenAI 允许 Fable 利用 GPT-3 创建虚拟人物需要一些谨慎。“我们非常有兴趣让我们的角色作为角色与人交谈，”Carey 说。“你可以想象，这可能是他们的一个问题领域，对吧？[它]肯定有可能被某人假装成人类而被恶意使用。”Fable Studio 和 OpenAI 团队花了一些时间解决创建逼真角色和模仿人类之间的区别，然后 OpenAI 批准了 Fable 的用例。

OpenAI 还有另一个要求：在任何虚拟实体在观众面前假装“真实”进行叙述实验时，Fable 团队必须在过程中保持人类参与其中。根据 Carey 的说法，让 GPT-3 在面向数千人的体验中发挥作用是具有挑战性的。尽管如此，他仍然认为大型语言模型将会是一个福音，“即使用于预先撰写内容或在更宽容的领域中‘实时’使用且没有限制。”

Carey 认为，GPT-3 作者最好将其作为协作工具交到擅长讲故事艺术的人手中，这样可以获得更好的结果，而不是期望 GPT-3 完成所有工作。

谈及成本时，他认为故事讲述用例面临的挑战是，每次 API 请求都要保持 GPT-3 与发展中的故事一致，必须“提供所有细节并生成一些补充内容。所以仅仅生成几行，你就被收取了整个 token 集的费用。这可能是一个挑战。”

Fable Studio 如何应对定价问题？工作室成功地大部分避开了这个问题，主要是通过预生成进行实验，“你预生成了一堆选项，然后可以使用搜索找到正确的选项来回复，” Carey 说。

他们还找到了降低 API 用户数量的方法：与其让一个庞大的观众通过人工智能与 Lucy 互动，“我们有点转向了一种模式，即 Lucy 实际上是在进行一对一的对话，但是在 Twitch 直播中。” 观众通过 Twitch 观看而不是发起 API 调用，这缓解了带宽问题，限制了 Lucy 在任何给定时间与人互动的人数，并扩大了观众群体。

Saatchi 提到了一个传闻，即 GPT-4 正在探索对虚拟空间的空间理解，他认为这比仅限于语言的聊天机器人具有更多潜力。他建议探索这种用例的人们专注于在虚拟世界中创建角色。Saatchi 指出，Replika 是一个创建了虚拟 AI 朋友角色的公司，现在正在探索进入元宇宙，其中虚拟实体将拥有自己的公寓，可以相遇并与其他人类用户以及最终与人类用户进行交互。“重点是要创造一个感觉活生生的角色，而 GPT-3 只是众多工具中的一种。为这些角色提供对他们正在导航的空间的真正理解可能会为这些角色带来学习的机会。”

未来会有什么？Carey 觉得未来版本的 GPT-3 在构建元宇宙方面有一席之地，元宇宙是一个平行的数字现实，人类可以像在真实世界中一样自由地交互和进行活动。他设想它能够生成想法，并让人参与其中以进行策划。

Saatchi 认为，将语言减弱为唯一的交互模式具有创造更有趣和复杂的与 AI 互动的潜力。“我确实认为 3D 空间为我们提供了让 AI 具有空间理解的机会，”他继续说道。Saatchi 所展望的元宇宙赋予了 AI 走动和探索的能力，同时也给了人类成为循环的一部分并帮助训练虚拟存在的机会。他总结道我们需要激进的新思维，并且元宇宙提供了在 3D 空间中放置 AI 角色和“允许它们与人类一起过模拟生活”的重大机会。

## GPT-3 的数据分析应用：Viable

创业公司[Viable](https://www.askviable.com)的故事是一个很好的例子，说明从开始着手一个商业理念到实际找到产品市场契合度和客户群体的过程有多大变化。Viable 通过使用 GPT-3 总结客户反馈来帮助公司更好地了解他们的客户。

Viable 汇总了诸如调查、帮助台票、实时聊天记录和客户评论等反馈。然后，它识别主题、情绪和情感，从这些结果中提取见解，并在几秒钟内提供摘要。例如，如果问到“我们的客户对结账体验感到沮丧的是什么？”Viable 可能会回答：“客户对结账流程感到沮丧，因为加载时间太长。他们还希望能够在结账时编辑地址并保存多种支付方式。”

Viable 最初的商业模式涉及帮助早期初创公司通过调查和产品路线图找到产品市场契合度。丹尼尔·埃里克森说，请求开始涌入来自更大公司的请求，要求支持分析大量的文本，如“支持票、社交媒体、应用商店评论和调查回复”改变了一切。埃里克森是 Viable 的创始人兼 CEO，也是 OpenAI API 的早期采用者。他解释说：“我实际上花了大约一个月的时间进行实验，简直就是将我们的数据放入 Playground 中，尝试不同的提示和类似的事物。最终，我得出了结论，[GPT-3] 可以驱动一个非常强大的问答系统。”

Erickson 和他的同事们开始使用 OpenAI API 与大型数据集进行交互并生成见解。他们最初使用了另一个自然语言处理模型，取得了平平的结果，但当他们开始使用 GPT-3 时，团队看到“在各方面至少有 10% 的增长。当我们说从 80% 提升到 90% 时，对我们来说是一个相当大的提升。”

基于这一成功，他们将 GPT-3 与其他模型和系统结合起来，创建了一个问答功能，允许用户用简单的英语提问并获得答案。Viable 将问题转换为一个复杂的查询，可以从数据库中提取所有相关反馈。然后，它通过另一系列的摘要和分析模型运行数据，生成精炼的答案。

此外，Viable 的系统每周为客户提供“一个由 12 段组成的摘要……概述了他们的主要投诉、主要赞美、主要请求和主要问题。”正如你可能期望的那样，作为客户反馈专家，Viable 在每个软件生成的答案旁边都有赞和踩按钮。他们将这些反馈用于重新训练模型。

人类也是这个过程的一部分：Viable 有一个标注团队，他们负责构建训练数据集，包括内部模型和 GPT-3 微调的数据集。他们使用当前版本的微调模型生成输出，然后由人类评估其质量。如果输出不合理或不准确，他们会重新写。一旦他们有了满意的输出列表，他们就会将该列表反馈到下一个训练数据集的迭代中。

Erickson 指出 API 是一个巨大的优势，因为它将托管、调试、扩展和优化留给了 OpenAI：“对于几乎与我们的技术无关的任何事情，我更愿意购买而不是构建。即使对我们的技术至关重要，使用 GPT-3 也是有意义的。”因此，他们的理想解决方案是将 GPT-3 用于其流程的所有元素。但由于成本问题，他们不得不优化其使用：“我们有一些公司向我们提供数十万个数据点，每个数据点长度从五到一千个单词不等。”将 GPT-3 用于一切可能会很昂贵。

相反，Viable 主要使用内部模型来构建数据结构，这些模型是建立在 BERT 和 ALBERT 之上的，并使用 GPT-3 的输出进行训练。这些模型现在在主题提取、情感分析和许多其他任务方面达到或超过了 GPT-3 的能力。Viable 还切换到了基于使用量的价格模型，该模型建立在 OpenAI 的 API 价格之上。

Erickson 坚称 GPT-3 在准确性和可用性方面给 Viable 带来了竞争优势。我们已经提到了 Viable 令人印象深刻的 10% 的准确度提升。但可用性如何呢？Viable 的大多数竞争对手都构建了专门为专业数据分析师设计的工具。Viable 觉得这个受众太狭窄了：“我们不想构建只有分析师才能使用的软件，因为我们觉得那样会限制价值。我们想做的是帮助团队使用定性数据做出更好的决策。”

相反，Viable 的软件本身就是“分析师”。用户可以通过自然语言迭代更快，这要归功于一个反馈循环，允许他们用自然语言提问关于他们的数据的问题，并获得快速准确的回答。

Erickson 分享了 Viable 的一些下一步计划：它将很快引入量化数据和分析产品分析。最终，Erickson 想要给用户提供进行全面客户洞察分析的能力，并提出诸如“有多少客户正在使用功能 X？”和“使用功能 X 的客户中，他们认为应该如何改进？”等问题。

最终，Erickson 总结道：“我们销售的是生成的见解。因此，我们使这些见解越加深入和强大，以及我们越快地传递这些见解，我们就创造了越多的价值。”

## GPT-3 的聊天机器人应用：Quickchat

GPT-3，作为一种非常擅长语言交互的技术，是增强现有聊天机器人体验的明显选择。虽然许多应用程序通过 AI 聊天机器人角色来娱乐用户，比如[哲学家 AI](https://philosopherai.com)和[Talk Kanye](https://talktokanye.com)，但有两家公司特别利用这一能力在其业务应用中：Quickchat 和 Replika。Quickchat 以其 AI 聊天机器人角色 Emerson AI 而闻名，可通过 Telegram Messenger 和 Quickchat 移动应用访问。Emerson AI 拥有广泛的世界知识，包括对比 GPT-3 用于训练的更多近期信息的访问；支持多种语言；能够进行连贯的对话；而且很有趣。

Quickchat 的联合创始人 Piotr Grudzień和 Dominik Posmyk 对 GPT-3 从一开始就充满了兴奋，并且对在新产品中利用它充满了想法。在他们早期对 OpenAI API 进行的实验中，他们一直在思考“机器和人之间的界面的演变”这个概念。Grudzień解释说，由于人与计算机之间的交互不断发展，自然语言将是合乎逻辑的下一步：毕竟，人们更喜欢通过对话进行交流。他们得出结论，GPT-3 似乎有潜力实现与计算机进行类似人类的聊天体验。

格鲁吉涅说，创始人中没有一个人曾经构建过传统的聊天机器人应用程序。以“初学者的心态”对待这项任务帮助他们保持清新，并对解决问题持开放态度。与其他聊天机器人公司不同，他们并没有开始时就有成为最佳客户支持或营销工具的野心。他们最初思考的是：“如何让一个人以令人敬畏的方式与机器交谈，并且是他们尝试过的最好的事情？”他们想要制作一个不仅完成简单功能（如收集客户数据和提供答案），而且还能准备回答非脚本化的客户问题或进行愉快的闲聊的聊天机器人。“而不是说‘我不知道’，”格鲁吉涅补充道，它可以“借助对话 API 并继续对话。”

波斯米克补充道：“我们的使命是赋予人们人工智能，而不是取代他们。我们相信，在未来的十年里，人工智能将加速教育、法律、[和]医疗等关键行业的数字化，并提高我们在工作和[日常生活中]的生产力。”为了展示这个遥远的使命，他们创建了 Emerson AI，一款由 GPT-3 提供支持的智能通用聊天机器人应用程序。

尽管 Emerson AI 拥有日益壮大的用户社区，但其真正目的是展示由 GPT-3 提供支持的聊天机器人的能力，并鼓励用户与 Quickchat 合作为其公司实施这样的角色。 Quickchat 的产品提供是一款通用的对话人工智能，可以谈论任何主题。客户，主要是成立已久的公司，可以通过添加特定于其产品（或任何他们想要的主题）的额外信息来定制聊天机器人。Quickchat 已经看到了多样的应用，例如自动化典型的 FAQ 客户支持问题解决以及实施一个 AI 角色来帮助用户搜索内部公司知识库。

与典型的聊天机器人服务提供商不同，Quickchat 不会构建任何对话树或刚性场景，也不需要教导聊天机器人以特定方式回答问题。相反，格鲁吉涅解释说，客户遵循一个简单的流程：“您复制粘贴包含您希望您的 AI 使用的所有信息的文本 [然后] 点击重新训练按钮；[它] 需要几秒钟来吸收知识，就这样。”现在经过数据训练的聊天机器人已经准备好进行测试对话了。

谈到开源模型和 OpenAI API 之间的权衡，Grudzień分享道，“OpenAI API 很好用，因为你不需要担心基础架构，延迟或模型训练。它只是调用一个 API 并得到一个答案。它非常可靠。”但是，他认为你为质量付出了相当高的代价。相比之下，开源模型似乎是一个很好的免费选择。实际上，“你确实需要支付云计算的成本。它需要 GPU 和设置 GPU 以使这些模型快速工作，然后对你自己的模型进行微调，” Grudzień承认，这并不是一个琐碎的过程。

像 Viable 的 Erickson 一样，Grudzień和 Posmyk 努力在每一个 API 调用中提供价值。但他们也希望随着越来越多的竞争性模型的发布，OpenAI 的 API 定价会“下降或者会达到某个水平，仅仅是因为竞争的压力。”

Quickchat 学到了什么？首先，要建立一个盈利的业务，需要的不仅仅是炒作。像推出 GPT-3 那样的大型媒体轰动可以为激动人心的爱好者提供初步的涌入，"但是人们会感到厌倦，等待下一个大事件。唯一能生存下来的产品是那些真正解决了人们关心的问题的产品，" Grudzień说。“没有人会仅仅因为它是 GPT-3 就使用你的产品。它需要提供一些价值，无论是有用的还是有趣的，或者解决一些问题。GPT-3 不会为你做到这一点。所以你需要把它当作又一个工具来对待。”

另一个关键的教训是制定可靠的性能指标。“每当你构建一个机器学习产品时，评估都是棘手的，” Grudzień说。在他看来，由于 GPT-3 是强大的，并且在难以量化的自然语言领域运作，评估其输出质量是复杂且繁琐的。正如突破性的东西一样令人兴奋，他说，“用户可能会根据你最差的性能来评判你，最好是根据你的平均性能。”因此，Quickchat 优化了用户满意度。对于公司来说，设计一个能捕捉与用户满意度和高留存率相关的变量的度量标准至关重要，这两者直接转化为更高的收入。

另一个挑战，也许出乎意料的是 GPT-3 对创造力的嗅觉。“即使你将温度设定得非常低，你给它提供的提示它仍然会使用非常小的提示，然后基于它拥有的广泛知识生成一些东西，” Grudzień解释道。这使得它很容易生成诸如诗歌、营销文案或幻想故事等创意文本。但大多数聊天机器人都是用来解决客户问题的。“它需要有可预测的、重复的性能，同时还需要有对话性和在某种程度上的创造性，但不要推得太远。”

大型语言模型有时会输出“奇怪的”、“空洞的”或者“不那么好的”文本，因此需要人类干预。“如果你开始衡量它是否满足了某些条件或者完成了任务，那么它会被证明非常有创意，但在十次尝试中，它只成功了六次——对于有付费客户的实际业务来说，这就相当于零。” 因此，要实现成功的业务应用，你需要许多内部系统和模型来限制创意并提高可靠性。“为了为我们的客户创建一个 99% 时间正常工作的工具，我们开发了许多防御机制，”格鲁吉尼说。

这些天，Quickchat 致力于与客户深入合作，确保他们的 API 性能使他们在使用案例中取得成功。格鲁吉尼最兴奋的是看到客户构建的东西：“我们真的非常希望看到我们的聊天引擎在成千上万种不同的方式中被用于不同的产品中。”

## GPT-3 的营销应用：Copysmith

GPT-3 能消除写作困境吗？YouTuber 亚尼克·基尔彻认为可以：“如果你遇到写作困难，只需向模型询问，它会提供数百个想法作为倾听板。” 让我们来看看一个这样的工具：Copysmith。

GPT-3 最受欢迎的应用之一是即时生成创意内容。Copysmith 是市场上领先的内容创作工具之一。“Copysmith……通过强大的人工智能，使用户能够在网络上创建和部署内容的速度提高一百倍，”联合创始人兼首席技术官安娜·王说道。它利用 GPT-3 在电子商务和营销领域进行文案撰写，以实现高质量内容的快速生成、协作和发布。王和首席执行官谢贡·奥图拉纳分享了两姐妹如何将他们的小型电子商务店转型为成功的科技公司——而 GPT-3 在其中发挥了关键作用。

2019 年 6 月，安娜·王和她的姐姐茉莉花·王共同创立了一个基于 Shopify 的精品店。但她们缺乏营销经验，“生意彻底垮了，”安娜·王说。当姐妹俩在 2020 年了解到 OpenAI API 时，王说：“我们开始探索它用于写作诗歌、模仿书籍和电影中的人物等创意追求。有一天我们意识到，如果我们在尝试建立电子商务店时有了这个工具，我们就能写出更好的行动号召和产品描述，提升我们的营销水平，让其起步。”

受启发，他们于 2020 年 10 月推出了 Copysmith 并受到热烈欢迎。在王的话中，“一切都从那里开始。我们开始与用户交流，并根据反馈迭代产品。” 她指出，GPT-3 使得你可以在没有任何先前知识的情况下迅速进行迭代，而其他开源模型，比如 BERT 和 RoBERTa，需要针对每个下游任务进行大量微调。她补充说：“它在执行任务方面极其灵活”，还说“它是目前最强大的模型。” 此外，GPT-3 对开发人员和用户来说“非常友好”，其简单的“留言输入，留言输出”接口允许你使用一个简单的 API 执行各种任务。” 它的另一个优点是 API 调用的简单性，与承载专有模型的努力相比要简单得多。  

关于基于 GPT-3 构建产品的挑战，Otulana 表示：“通常情况下，你受限于 OpenAI 的限制。因此，要克服这一点，你必须为 API 加入自己的创业元素，以创建出与众不同的东西。另一个限制是稍微失去控制，你的进展实质上受到 OpenAI 进展的限制。”  

王对想要使用 GPT-3 的产品设计师有两条建议。首先，她说：“确保你正在解决一个真正的问题……考虑你的用户，因为使用 GPT-3 的一个容易出现的问题是陷入只在安全准则的限制内构建东西的思维定式，而不允许自己有创意。”

王建议说：“第二，要非常密切地关注你输入到模型中的内容。小心标点符号、语法和提示的措辞。我向你保证，你会对模型输出有更好的体验。”  

## GPT-3 的编码应用：Stenography  

随着 GPT-3 及其后代模型 Codex 展现出与编程和自然语言交互的能力，新的潜在用例正在堆积起来。  

OpenAI 社区大使 Bram Adams 以他与 GPT-3 和 Codex 算法进行创造性实验而闻名，在 2021 年底推出了一个产品：Stenography，利用 GPT-3 和 Codex 来自动化写代码文档这一讨厌的任务。Stenography 立刻取得成功，在热门产品发布门户 Product Hunt 上当日成为第一产品。  

Adams 在缩小想法范围之前尝试了 API 的几个潜在用例，其中一个成为了他的新业务。“我认为很多这些实验都是我无意识地对 GPT-3 这样的语言模型能处理什么进行边缘测试。” Adams 的搜索始于这样一个想法：“如果我可以让计算机做任何事情，我会怎么做？”他开始探索，“触摸 OpenAI API 的边缘，看看它能走多远。” 他开发了一个生成 Instagram 诗歌的机器人；尝试了一个自我播客日记项目，用户可以与自己的数字版本交谈；基于用户偏好，在 Spotify 上构建音乐播放列表的项目；以及在满足好奇心的过程中创建了许多其他项目。由于这种好奇心，“我很早就擅长理解 GPT-3 的不同引擎。”

那么为什么选择隐写术呢？“我从外界获得了一个相当好的信号，表明这对很多人可能非常有帮助。” 虽然 Adams 喜欢精心编写的代码的优雅之处，但大多数 GitHub 用户只是下载已发布的代码并使用它：“没有人真的会欣赏你在代码库中付出的美感。” 他还注意到，GitHub 上很棒的程序如果没有很好的文档说明往往不会得到应有的关注：“readme [文件] 是每个人都会看到的第一件事。他们会立即向下滚动查看。” 隐写术是一种思考文档如何发展以减少对开发人员来说变得不那么烦人的尝试：“这很难，因为特别是文档，你必须证明你的做法。所以你说，‘我使用这个库来做这件事。然后我决定使用这个东西，然后我添加了这个函数来做这个事情。’”

Adams 将文档视为人们与团队其他成员、未来的自己或者只是偶然发现该项目的感兴趣的人交流的一种方式。其目标是让项目对他人易于理解。“我对 GPT-3 能否创建易于理解的评论的想法很感兴趣。” 他尝试了 GPT-3 和 Codex，并对两种模型的解释水平印象深刻。他接下来问的问题是：“如何使这对开发人员来说真的变得简单和愉快？”

那么隐写术是如何工作的，其组件如何利用 OpenAI API？Adams 表示，从高层次来看，有两个主要的过程——解析和解释——每个过程都需要不同的策略。“对于解析过程，我花了很多时间理解代码的复杂性，因为你的代码中并不是每一行都值得记录。” 一些代码可能有明显的目的，没有操作价值，或者不再有用。

此外，“大”代码块，超过 800 行，对模型来说太棘手了。 “你必须将逻辑拆分成许多不同的步骤，才能准确地说出这个东西是干什么的。一旦我理解了这一点，我就开始思考，‘我该如何利用解析来找到足够复杂但又不太复杂的块？’” 由于每个人的代码编写方式都不同，所以问题在于试图连接到抽象语法树，并尽力利用你所拥有的最好的东西。这成为了解析层的主要架构挑战。

至于解释层，“这更像是让 GPT-3 和 Codex 说出你想要它们说的话的一个功能，” Adams 解释道。解决这个问题的方法是找到创造性的方式来理解你代码的受众，并让 GPT-3 向他们表达。这个层面“可以尝试解答任何问题，但可能不会像使用计算器那样百分之百准确。如果你输入两加二等于四，偶尔会得到五，但你不需要编写所有的乘法、除法和减法函数。这些是免费的。” 这就是概率系统的取舍：有时候它们有效，有时候不行，但它们总会返回 *一个* 答案。Adams 建议保持足够灵活，以便在必要时调整你的策略。

Adams 强调在开始使用 OpenAI API 前真正理解问题的重要性。“在我的办公时间里，人们会来找我，他们会遇到这些巨大的问题。他们会说，‘我怎样才能用一行提示建造一艘火箭？’ 我会说，‘嗯，火箭有很多部件。GPT-3 不是万能药。它是一台非常强大的机器，但只有当你知道你在用它做什么时才有效果。’” 他将 GPT-3 比作 JavaScript、Python 和 C 这样的编程语言：“它们很吸引人，但前提是你要理解递归和 `for` 循环以及 `while` 循环，以及哪些工具能帮助你解决你特定的问题。” 对于 Adams 来说，这意味着要问很多“技术元问题”，比如“有了 AI 文档，会帮助到什么程度？” 和 “文档到底是什么？” 处理这些问题是他面临的最大挑战。

“我认为很多人会立刻求助达芬奇来解决问题。但如果你能用一个较小的引擎解决问题，比如 Ada、Babbage 或者 Curie，你实际上会比仅仅试图用达芬奇的整个 AI 来解决问题更深入地了解问题。” 他声称。

当涉及到使用 OpenAI API 构建和扩展产品时，他建议使用“小引擎或低温度”，因为你无法预测最终提示会是什么样（或者它是否会随时间而演变）、你试图做什么以及最终用户是谁，但是通过使用较小的引擎和较低的温度，你将更快地找到对真正困难的问题的答案。”

另一个挑战是从他自己的独立实验转变为一个应用程序，考虑到用户可能面临的所有不同条件和工作方式。现在，他正在致力于“找到所有不同的边缘情况”，以更好地了解 API 的设计层必须有多快，它必须以多频繁地响应特定请求，以及它如何与不同的语言交互。

对于速记术的下一步是什么？现在亚当斯已经建立了一个他非常满意的产品，他计划在 2022 年专注于销售和与用户群体交流。“速记术不会像以前那样多地关注建设，而是更多地关注真正完善产品并让其为人们所熟知。”

# 投资者对 GPT-3 初创企业生态系统的看法

为了了解支持基于 GPT-3 的公司的投资者的观点，我们与 Wing Venture Capital 的 Jake Flomenberg 进行了交流，该公司是一家著名的全球风险投资公司，也是几家以 GPT-3 为动力的初创企业，包括 CopyAI 和 Simplified 的主要投资者。

如同任何市场观察者可能想象的那样，风投资本家正在关注 GPT-3 等新兴人工智能技术。Flomenberg 总结了其吸引力：GPT-3 是“我们以前从未见过的任何其他 NLP 模型。它是朝着构建更通用的人工智能迈出的实质性一步。”他认为未开发的潜力是巨大的，并且商业世界仍然“低估了并因此未充分利用 LLMs 的能力。”

那么潜在投资者应该如何评估这么新颖和不同的东西呢？Flomenberg 说：“我们看重对问题、领域和技术的深入理解的初创企业，以及展示产品与市场之间良好契合度的初创企业。”“评估建立在 GPT-3 上的东西的微妙之处在于，询问，秘密酱是什么？公司是否在技术上对某事有深入的了解？公司是在使用 GPT-3 解决了一个真正的问题，还是只是利用炒作将其产品推向市场？为什么现在？为什么这个团队是最适合执行这个想法的？这个想法在现实世界中是可防御的吗？”如果一个初创企业无法为自己的存在辩护，那对投资者来说是一个巨大的警告信号。

投资者们也在密切关注 OpenAI 及其 API，因为基于 GPT-3 的企业完全依赖于其能力。Flomenberg 将 OpenAI 的尽职调查审查过程视为这种基于信任的关系的重要因素：“通过了生产审查并受到 OpenAI 关注的初创企业自动成为投资的热门对象。”

投资者在做出投资决策时通常会深入了解创始人的背景和专业知识。然而，GPT-3 不同寻常，因为它允许来自任何背景，而不仅仅是程序员的人，构建尖端的自然语言处理产品。弗洛门伯格强调了市场的重要性：“通常情况下，对于一家深科技初创公司，我们寻找对技术和人工智能领域有着深刻理解的创始人。但是对于基于 GPT-3 的初创公司，我们更关注市场是否 resonates with the founders’ vision 以及他们是否能够识别和解决最终用户的需求。” 他引用 CopyAI 作为 “建立在 GPT-3 之上的产品导向增长模式的典型例子。他们与用户之间建立了非凡的共鸣，并深入了解了技术，为业务带来了深度和价值。” 他说，成功的初创公司 “将 AI 保持在内部”，更专注于通过使用适当的工具解决用户的问题并满足他们的需求。

# 结论

看到这些用例以及许多其他用例如此迅速地以及如此成功地构建在 GPT-3 之上，令人惊叹。到 2021 年末，即写作本章时，开放 AI 社区中已经有几家初创公司筹集了大量资金，并且正在考虑快速扩张计划。这股市场潮流似乎也唤醒了更大型企业的胃口。越来越多的企业开始考虑在其组织内实施实验性的 GPT-3 项目。在 第五章 中，我们将研究这个由像 GitHub Copilot 和特别是新的 Microsoft Azure OpenAI Service 这样的大规模产品组成的市场细分，该服务旨在满足大型组织的需求。

^(1) 请参阅 IBM 网站上的文章 [“AI 创造力的追求”](https://oreil.ly/QM7kk)。

^(2) 简要解释，请查看 OpenAI 的 [这篇博文](https://oreil.ly/ksvwe)；深入了解，请参阅开发团队的 [研究论文](https://oreil.ly/8wpcs)。

^(3) 您可以在 Vimeo 上观看 *德古拉* [on Vimeo](https://oreil.ly/hnHaf)。

^(4) *Metaverse* 在这个语境中指的是一个未来主义概念，即由填满了社交连接的虚拟头像的 3D 虚拟世界网络。这个更广泛的概念独立于马克·扎克伯格关于元宇宙的愿景。
