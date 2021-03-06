[#]: collector: (bestony)
[#]: translator: (gxlct008)
[#]: reviewer: (windgeek)
[#]: publisher: ( )
[#]: url: ( )
[#]: subject: (Command Line Heroes: Season 3: Creating JavaScript)
[#]: via: (https://www.redhat.com/en/command-line-heroes/season-3/creating-javascript)
[#]: author: (RedHat https://www.redhat.com/en/command-line-heroes)

Command Line Heroes: Season 3: Creating JavaScript
======

**00:00** - _Saron Yitbarek_

嗨，大家好。 我们回来了。 我们很高兴能推出 Command Line Heroes 第三季。 我们要感谢你们中很多人在这个节目中讲述的故事，因为每一季都源于我们与开发人员、 SIS 管理员、 IT 架构师、 工程师以及开源社区的人们讨论您最感兴趣的的主题和技术。 现在，我们正在进一步开放这种方式。 我们希望大家都能参与进来，帮助塑造 Command Line Heroes 的未来。 您可以通过我们的简短调查来做到这一点。 您喜欢这个节目的什么地方？ 您还希望我们多谈论哪些内容？ 亲爱的听众，我们想进一步了解您。 您是开发人员吗？ 您是在运营部门工作，还是在做一些与技术完全无关的工作？ 请访问 commandlineheroes.com/survey，以帮助我们提升第四季及以后的播客内容。 现在，让我们进入第三季。

**01:00** - _Saron Yitbarek_

Brendan Eich (布兰登·艾奇) 在 Netscape (网景) 公司总部的办公桌前坐下时只有 34 岁。 他正致力于为期 10 天的大规模编码冲刺。 一种新的语言，一种全新的编程语言，将在在短短 10 天内诞生。 那是在 1995 年，编程语言的世界即将永远改变。

**01:26** - _Saron Yitbarek_

我是 Saron Yitbarek，这里是 Command Line Heroes，一个来自 Red Hat (红帽) 的原创播客。 整个一季，我们都在探索编程语言的威力和前景，探索我们的语言是如何塑造开发世界的，以及它们是如何推动我们的工作的。 这一次，我们追踪 JavaScript 的创建历程。 也许您以前听过 Brendan Eich 的故事，但是像 JavaScript 这种计算机语言是如何真正创造的呢？ 其中肯定有 Brendan 的冲刺。 但是这个故事还有更多的内容。

**02:02** - _Saron Yitbarek_

我们的 JavaScript 故事始于一场战争，一场浏览器之战。 1990 年代的浏览器大战似乎已经成为历史，但他们的影响无疑是巨大的。 在战场的一方，Netscape 与 Sun Microsystems 结成了联盟。 另一方，您看到的是 Microsoft，软件巨头。 他们争夺的战利品是什么？ 赌注已经大得不能再大了，因为这是一场决定谁将成为互联网看门人的对决。 

**02:40** - _Saron Yitbarek_

为了真正了解浏览器之战是如何落下帷幕的，让我来打电话给我最喜欢的科技历史学家之一、 作家 Clive Thompson (克莱夫·汤普森)。 他最新的一本书——

**02:50** - _Clive Thompson_

《编码者: 新部落的形成和世界的重塑》。

**02:54** - _Saron Yitbarek_

Clive 和我谈论的是浏览器之战，让我来为您做个铺垫吧。 您会看到 Netscape 意识到浏览器将会是人们用来上网的关键软件。 还有 Microsoft，他们的整个商业模式就是将东西打包到 Windows 中。 直到 1990 年代，他们才真正对浏览器感兴趣，微软意识到也许他们一直睡在方向盘上了。 世界正在向线上移动，微软 Windows 内没有任何东西可以帮助他们实现这一目标。 但是那里的那些人，一家名为 Netscape 的公司，他们正在提供一个通往互联网的入口。 突然之间，微软在整个行业的主导地位看起来并不是那么绝对。 浏览器之战始于那一刻，即微软意识到了互联网的力量，并眯着眼睛看向他们新竞争对手的那一刻。 好了，这就是我的铺垫。 这里我和 Clive 讨论接下来发生的事情。

**04:03** - _Clive Thompson_

这场战争是关于谁将成为上网的主要门户。 您必须意识到，在 90 年代初期，没有人真正在线。 当 Mosaic 出现并最终变成 Netscape 时，他们是第一款任何人都可以下载的并让人能够浏览Web的浏览器。 他们于 1994 年 12 月上线。 所以突然之间，成千上万的人能够以这种图形方式使用互联网。 他们获得了巨量的下载和大量的新闻报道。 基本上每个人都在说：“是的，Netscape 是这种被称之为互联网的事物的未来。”

**04:40** - _Clive Thompson_

所以在西雅图，你可以看到微软非常警惕地关注着这件事，因为他们几乎忽略了互联网。 他们只专注于销售 Windows，实际上并没有对这种被称为互联网的疯狂新事物给予任何关注。 因此，他们不得不玩一场急速追赶游戏。 近一年后，他们才推出自己的浏览器。 在 1995 年秋天，他们的浏览器问世了，这实质上是浏览器大战的开始，那时微软也正在努力成为人们上网的门户。

**05:13** - _Saron Yitbarek_

Okay。 花费一年的时间才让浏览器面世听起来不算太糟，对吧？ 时间不算太长。 对吧？ 这似乎是一个合理的时间。

**05:21** - _Clive Thompson_

不，是真的。 这听起来好像不是很长时间，但那时事情发展得是如此之快。 而且人们有一种强烈的先发优势意识，那就是第一家能以你上网的方式作为自己品牌的公司将成为多年的赢家，甚至可能永远是赢家。 我还记得当时的开发速度有多快。 我的意思是，Netscape 每两三个月就会推出一款新的浏览器，对吗？ 他们会说，“哇。 现在，我们已经将电子邮件集成到浏览器中了。 现在，我们在顶部有了一个小小的搜索栏。” 它一直在变得越来越好。 你可以在某种程度上看到，你知道的，可以在网上做的所有事情都进入了视线，因为它们可以快速迭代并快速将其推出。

**06:01** - _Clive Thompson_

微软习惯于非常缓慢的开发模式。 这是您长达四年的开发过程。 它是我们能买到的没有 bug 的版本。 把它封盒，投放到商店去，然后我们四年都不发布新版本。 现在 Netscape 出现了，它是第一家说，“不，我们将推出一款不怎么合格的产品，但它运行得足够好，我们将在三个月、三个月又三个月内推出一个新的供你下载。” 这完全破坏了微软的稳定。

**06:30** - _Saron Yitbarek_

好吧。 如果我是微软，我可以看着它说，“哦，天哪。 这就是未来。 我需要迎头赶上。 我需要竞争。” 或者我可以说，“啊，这是一种时尚。” 那么浏览器到底是什么？ 这让微软选择了第一个选项。 它让微软说，“哦，天哪。 这是真的。 我需要竞争。”

**06:51** - _Clive Thompson_

浏览器本身具有大量的文化传播和积淀作用。 您在互联网上可以做的第一件事，一般是获得像文化之类的乐趣。 您可以突然进入某个乐队的网页，查看他们的帖子和他们的照片。 您可以通过找到佛罗里达州的所有模特训练人去研究自己的爱好，对吗？ 所以，在此之前，关于互联网的一切都看起来很刻板。 电子邮件，文件传输，诸如此类。 我的意思是，突然之间，浏览器使互联网看起来像一本杂志，像一个有趣的互动对象。 报纸，CNN 和杂志第一次以这种非常激动人心的方式对此进行了报道。 就在这一刻，科技从深入商业版块发展成为 《纽约时报》 A1 版。

**07:41** - _Saron Yitbarek_

那么，对于开发人员而言，Netscape 甚至仅仅只算是浏览器能有什么吸引力呢？ 他们为什么如此着迷呢？

**07:48** - _Clive Thompson_

为此我拜访过很多开发人员。 突然间，随着浏览器的出现，互联网出现了，你可能只看到一个 web 页面，上面写着：“下载我那酷酷的软件吧。” 因此，它开启了我们今天看到的软件制造的整个世界。

**08:04** - _Saron Yitbarek_

我在这里应该提一下，起初微软实际上提出要收购 Netscape。 他们出价很低，Netscape 拒绝了他们。 因此，微软不得不打造自己的浏览器。 称他们自己的为 Explorer (IE)。

**08:21** - _Clive Thompson_


微软花了一年的时间疯狂地开发浏览器，并于 1995 年秋天将其推出。 他们所做的与 Netscape 差不多。 他们很快就做出了一些东西，并不担心它是否完美，因为它会越来越好。 但是，在 90 年代后半叶真正出现的是一场关于谁的浏览器将是最有趣，最具交互性、最尖端的战争。

**08:53** - _Saron Yitbarek_

请记住，Netscape 在这方面绝不占上风。

**08:57** - _Clive Thompson_

微软拥有非常强大的地位。 当 Windows 安装到全球所有计算机的 80％ ~ 90％ 时，很容易就会把您的软件设置为默认软件。 而这正是他们所做的。 所以你可以看到 Explorer 的崛起，崛起，崛起。

**09:16** - _Saron Yitbarek_

在某种程度上，可怜的老网景在这场战斗中一直处于劣势，但事情就是这样。 在战斗结束之前，他们抛出了一个美丽的 Hail Mary，事实证明，这将成为整个编程世界的一个令人难以置信的成绩。

**09:35** - _Clive Thompson_

这就是 JavaScript 创建过程中迷人而怪异的故事。

**09:43** - _Saron Yitbarek_

所有围绕网络的热议，围绕浏览器生命潜力的热议，都非常清楚地表明了一件事。 我们需要一种新的编程语言，一种远远超出 HTML 的语言。 我们需要一种为所有新的基于  web 的开发量身定做的语言。 我们想要一种不仅在线上生存，而且在那里蓬勃发展的语言。

**10:10** - _Clive Thompson_

如何为浏览器创建编程语言？

**10:15** - _Saron Yitbarek_

我的朋友，这是一个数十亿美元的问题。 大约在 Netscape 看到微软与他们竞争的时候，他们开始关注 Java™。 Java 会成为 Web 开发的语言吗？ Java 是这种丰富的编译语言。 它的性能和 C++ 一样好。 但它仍然需要编译。 开发人员确实想要一些更轻量级的东西，一些可以解释而不是编译的东西，一些可以吸引所有涌入 Web 的非专业程序员的东西。 毕竟，那些新的程序员想要直接在网页上工作。 那是梦想。

**11:05** - _Saron Yitbarek_

Netscape 需要一种可以在浏览器内部运行的编程语言，让开发人员能够让这些静态网页栩栩如生。 他们想，如果他们能在发布 Netscape 2.0 测试版的同时，发布一种新的轻量级语言，为网络编程创造奇迹，那不是很棒吗？ 只有一个问题。 他们正好有 10 天的时间来创造一门新的语言。 实际上，它给了一个叫 Brendan Eich 的人 10 天的时间。 他就是那个负责完成这件事的人。 毫无疑问，如果有人能做到这一点，那就是他。 当 Brendan 还是伊利诺伊大学的学生时，他常常为了好玩而创造新的语言，只是为了玩玩语法。

**11:57** - _Charles Severance_

Brendan Eich 的关键在于，那时的 Brendan Eich，在构建 JavaScript 时已经成了某种程度上的语言狂热分子。

**12:05** - _Saron Yitbarek_


为了了解 Eich (布兰登·艾奇) 到底取得了什么成果，我们联系了密歇根大学信息学院的教授 Charles Severance (查尔斯·塞维兰斯)。

**12:14** - _Charles Severance_

JavaScript 在某种程度上是在 Java 被视为未来的环境中创建的，在 1994 年，我们认为它 (Java) 将解决所有问题。 一年后，真正能解决一切的东西即将出现，但它不能说，“嘿，我已经解决了一切”，因为每个人，包括我自己，就像都相信 94，95 年我们看到了摇滚乐的未来一样，这个未来就是 Java 编程语言。 他们必须建立一种看似无关紧要，看似愚蠢，看似毫无意义，但却是正确的解决方案的语言。

**12:56** - _Saron Yitbarek_


但是 Eich 提供的可不仅仅是一种玩具语言。 它以隐藏的方式进行了复杂处理，并从以前的语言中汲取了主要灵感。

**13:07** - _Charles Severance_

如果您看一下基本语法，很明显它的灵感来自于带有花括号和分号的 C 语言。 一些字符串模式取自 Java 编程语言，但面向对象的底层模式取自名为 Moda-2 的编程语言，它有函数是一等类的概念。 对我来说，这确实是使 JavaScript 成为如此强大以及可扩展语言的最令人惊叹的选择之一，即函数的主体，构成函数本身的代码也是数据。

**13:41** - _Charles Severance_

另一个真正的灵感来源于 HyperCard。 JavaScript 总是在浏览器中运行，这意味着它有文档对象模型的基本数据上下文，文档对象模型是网页的面向对象表示。 它不像传统的编程语言。 JavaScript 代码不是从一开始就启动的。 首先它是一个网页，它最终也以这个面向事件的编程结束。

**14:12** - _Saron Yitbarek_

1995 年 11 月 30 日，当 JavaScript 与 Netscape Navigator 2.0 一起发布时，所有的魔力都被植入到一种强大的语言小种子中。 包括 America Online (美国在线) 和 AT&T (美国电话电报公司) 在内的 28 家公司同意将其作为一种开放标准语言使用。 当它发布时，有一些老的专业人士对 JavaScript 嗤之以鼻。 他们认为这只是一种新手的语言。 他们错过了它革命性的潜力。

**14:46** - _Charles Severance_

Brendan（布兰登）决定将所有这些来自不太知名语言的超高级概念融入其中，这些语言非常类似于高级面向对象语言。 所以 JavaScript 就像一只特洛伊木马。 它在某种程度上潜入了我们的集体意识，认为它是愚蠢的、 开玩笑的、 容易的和轻量级的。 但是几乎从一开始它就是内置的、 功能强大的、 深思熟虑的编程语言，它几乎能够在计算机科学中做任何事情。

**15:17** - _Saron Yitbarek_

其结果是成为了一种浏览器原生语言，可以随着我们在线生活的发展而不断进化。 没过多久，JavaScript 就成为了实际上的 web 开发选择。

**15:29** - _Charles Severance_

JavaScript 是一种我别无选择的语言，我只能学习它，从字面上讲，学习 JavaScript 的人通常别无选择，因为他们会说，“我想构建一个浏览器应用程序，我想让它有交互元素。” 因此，答案是您必须学习 JavaScript。 如果你想象一下，比如说，你最喜欢的语言是什么，那么这个问题的答案几乎就是 x 加上 JavaScript，对吧？ 有人可能会说，“我喜欢 Python 和 JavaScript ”，或者 “我喜欢 Scala 和 JavaScript”，因为它就像是每个人都需要学习的语言。

**16:05** - _Saron Yitbarek_

Charles Severance (查尔斯·塞维兰斯) 是密歇根大学信息学院的教授。 他说，Netscape 公司一开始非常强大，他们在浏览器之战中奋力拼搏，但最终......

**16:22** - _Clive Thompson_

Netscape 作为一款严肃的产品就这样消失了。

**16:27** - _Saron Yitbarek_

微软在整个行业的主导地位是一股压倒性的力量。 尽管在浏览器游戏上晚了一年，但他们还是能够重新站上榜首并赢得了这一天的胜利。 但你知道，Netscape 的 Hail Mary，它的 JavaScript 的创造，是成功的，因为在战斗结束很久之后，这种从浏览器战争中诞生的语言的瑰宝，它的来世将改变一切。

**17:01** - _Saron Yitbarek_

如果您是最近才开始编程的，很可能会认为您可以开发可更改和更新的交互式 Web 页面，而无需从服务器提取页面的全新副本。 但是，想像一下，当这样做会成为一种全新的选择时会是什么样子的。 我们有请 Red Hat (红帽公司) 的软件工程师 Michael Clayton (迈克尔·克莱顿) 帮助我们了解那是一个多么巨大的转变。

**17:28** - _Michael Clayton_

在，我想说 2004 年，Google Mail 发布了。 Gmail，据我所知，它是第一个真正将 JavaScript 带到更高水平的 Web 应用程序，它使用 JavaScript 来动态地切换你正在查看的内容。

**17:49** - _Saron Yitbarek_

假设您正在查看收件箱，然后单击了一封电子邮件。 在过去，你的电子邮件查看器会在你的浏览器中加载一个全新的页面，仅仅是为了向您显示那封电子邮件。 当您关闭该电子邮件时，它会重新加载整个收件箱。


**18:05** - _Michael Clayton_

这造成了很大的延迟。 当您在视图之间来回切换时有很多等待，Gmail 改变了这一切。 他们使用 JavaScript 在后台获取您想要查看的内容，然后将其展现在您面前，而无需等待全新的页面视图。

**18:23** - _Saron Yitbarek_

这节省了大量的时间和精力。 但是仔细想想，它改变的不仅仅是速度。 它改变了我们工作的本质。

**18:35** - _Michael Clayton_

所以，作为一种职业的 web 开发者，已经从类似幕后角色的服务端走到了离用户仅薄薄一层之隔的位置，因为他们直接在浏览器中编写代码，而用户也正是通过浏览器查看 web 页面。

**18:52** - _Saron Yitbarek_

它改变了一切。 事实上，您完全可以把引领 Web2.0 革命的功劳都归功于 JavaScript。 任何有网络浏览器的人都会突然之间拥有一个摆在他们面前的开发环境。 但是，正如我之前提到的，老保守派对民主程度并不一定感到舒服。


**19:16** - _Michael Clayton_

早期对 JavaScript 反对的，我也是其中的一员。 我有阻止 JavaScript 运行的浏览器扩展。 我认为它是一种无用的玩具语言，每当我访问一个网页，该网页的某些关键功能需要 JavaScript 时，我都会感到愤怒。 我想，“您应该在没有 JavaScript 的情况下以正确的方式构建您的网站。”

**19:43** - _Saron Yitbarek_

然而，很快，Brendan Eich 仅仅用 10 天创建的语言，它所蕴含的美和潜力对每个人来说都变得显而易见。 现在，它不仅征服了浏览器，也征服了服务器。 有了 Node.js，这种小语言可能会打开一个全新的领域。

**20:03** - _Michael Clayton_

当我听说 JavaScript 打算在服务器上运行时，我想，“为什么会有人想这么做？ 那时，我已经是一名专业的 JavaScript 开发人员了。 我每天都写很多 JS，但我还是不太明白为什么它可以归属到服务器端，事实证明，像很多听众都知道的那样，Node.js 现在是这个行业的一支巨大的力量。 我认为这是有充分理由的。

**20:32** - _Michael Clayton_

Node.js 如此成功的原因之一就是它挖掘到了庞大的前端 JavaScript 开发人员和客户端开发人员团体。 他们在写代码。 他们在用 JavaScript 为浏览器编写代码。 这么多的开发者，现在又可以用同样的语言来为服务器端编程，这让他们立刻就拥有了大量的可以立即开始为服务器端做贡献的人员。 该工具已经在您的工具包中，您只需将其拿出来，安装上 Node.js，然后就可以加入到编码竞赛中去了。

**21:11** - _Saron Yitbarek_


首先在浏览器中，然后又在服务器上。 JavaScript 是这种朴实无华、 暗地里优雅，有时候会有缺陷的语言。 一个所有人都低估了的浏览器战争的幸存者。

**21:25** - _Michael Clayton_

JavaScript 一直以来都是编程语言的灰姑娘故事，始于基本上是在 10 天内拼凑起来的初态。 中间经历了来自其他编程社区的许多嘲笑，然而仍以某种方式继续取得成功和增长，最后到现在稳居世界上最流行的编程语言中排名第一、第二的位置。 JavaScript 基本上无处不在。 在网页内部运行的能力意味着 JavaScript 和 Web 一样普及，这是非常普遍的。

**22:08** - _Saron Yitbarek_

Michael Clayton 是 Red Hat 的工程师。 JavaScript 吞噬了世界吗？ 它是否搭上了 web 的顺风车，才成了一种主流语言？ 我想找出 JavaScript 的实际边界在哪里。


**22:25** - _Klint Finley_

嗨，我叫 Klint Finley (克林特·芬利)。我是 Wired.com（连线）网站的撰稿人。

**22:28** - _Saron Yitbarek_

Klint (克林特) 对同样的事情也很好奇。 他越是关注今天 JavaScript 的运行方式，就越发意识到它已经渗透到他在线生活的每一个环节。

**22:40** - _Klint Finley_

甚至在您有机会决定是否希望所有这些不同的应用程序都在您的计算机上运行之前，JavaScript 已经成为一种可以增强整个应用程序能力的工具。 他们中的一些开始运行，他们参与了广告或促进广告商使用的跟踪。 所以，在你的浏览器中有很多事情是看不见的，你甚至可能不知道或者不想发生。

**23:07** - _Saron Yitbarek_

因此，Klint 决定进行一些实验。

**23:10** - _Klint Finley_

我决定试着在没有 JavaScript 的情况下使用 web 一段时间。 我决定试一试，花了一周时间禁用浏览器中的 JavaScript。

**23:21** - _Saron Yitbarek_

听起来很简单，但是放弃所有 JavaScript 产生了一些令人惊讶的效果。 因为 JavaScript 已经变得如此庞大，如此全方位耗费资源，这种以轻量级著称的语言现在实际上占用了大量的空间和精力。 当 Klint 屏蔽了那一种语言时才发现...


**23:39** - _Klint Finley_

总体而言，这在很多方面都是一种更好的 Web 体验，比如页面加载更快，页面更干净，我电脑的电池续航时间更长，并且我对电脑上发生的事情有了更多的控制感，因为并不是所有这些奇怪的、 看不见的随机程序都在后台运行。

**24:02** - _Saron Yitbarek_

想象一下第一次没有弹出式广告的生活是多么幸福。

**24:07** - _Klint Finley_

它在很大程度上依赖于 JavaScript 来加载。 所以网页变得简单多了，广告少了，干扰也少了。

**24:17** - _Saron Yitbarek_

不过，这种整洁的 web 体验并不是全部。 如果你拔掉 JavaScript 的插头，Web 的某些部分就完全不能工作了。

**24:26** - _Klint Finley_

很多内容都不能正常运行了。 我想 Gmail 把我重定向到了一个为旧手机设计的差异版本。 Facebook 做了同样的事情，很多流畅的互动没有了。 它变得更像是一系列的网页。 因此， Netflix 无法正常工作。 YouTube 无法正常运行。 是的，任何非常依赖互动的东西都不能运行了。 拿掉了 JavaScript，有好处也有坏处，最终我不得不做出抉择，有 JavaScript 总比什么都没有要好。

**25:05** - _Saron Yitbarek_

Klint Finley 是 Wired.com 的撰稿人。 大多数人预测 JavaScript 只会继续主导移动和桌面应用程序开发。 像基于浏览器的游戏、 基于浏览器的艺术项目等等，它们的复杂程度正在飞涨。 不断增长的 JavaScript 社区正在最大限度地利用这一潜力。

**25:34** - _Saron Yitbarek_

值得回想一下，就在 1995 年，就在几十年前，Brendan Eich 坐在一个房间里，设计出一门新的语言。 今天，这种语言渗透到我们所做的每一件事中。 说一些新的代码串将改变世界听起来有点陈词滥调，但它确实发生了。 一位代码英雄将他对语言的所有热爱汇聚到 10 天的冲刺中，世界的 DNA 也将永远改变。

**26:10** - _Saron Yitbarek_

我们可以为 Google Docs、 YouTube 和 Netflix 感谢 JavaScript。 但是您知道，“能力越大，责任越大”，随着 JavaScript 的影响力在大量开源库的推动下不断增长，责任不再仅仅落在一个人身上了。 范围更广的社区已经掌握了控制权。 SlashData 最近估计 JavaScript 开发人员的数量为 970 万，在 GitHub 上，JavaScript 比任何其他语言都有更多的 PR (Pull Requests) 。 力量在于整个世界的 Command Line Heroes，一直在帮助 JavaScript 在我们发展未来的过程中成长。

**26:59** - _Saron Yitbarek_

下一期，Command Line Heroes 将遇到另外一种 web 语言，我们将探索 Perl 是如何在一个广阔的新领域蓬勃发展的。

**28:04** - _Saron Yitbarek_

最后，一位听众分享了我们上一季的 Hello World 插曲，我们还谈到了 Brendan Eich 和 JavaScript。 在那一期，一位客人说，在那 10 天里，布兰登可能没有睡过多少觉，如果有的话，也是很少。 Brendan 在推特上回应说，他确实在那次冲刺过程中睡过觉。 想要更多地了解这 10 天发生了什么，请查看 Devchat 对 Brendan 的采访播客。 我们会在我们的节目记录里加个链接。 我是 Saron Yitbarek。 直到下期，请继续编码。


--------------------------------------------------------------------------------

via: https://www.redhat.com/en/command-line-heroes/season-3/creating-javascript

作者：[Red Hat][a]
选题：[bestony][b]
译者：[gxlct008](https://github.com/gxlct008)
校对：[windgeek](https://github.com/windgeek)

本文由 [LCRH](https://github.com/LCTT/LCRH) 原创编译，[Linux中国](https://linux.cn/) 荣誉推出
[a]: https://www.redhat.com/en/command-line-heroes
[b]: https://github.com/bestony

