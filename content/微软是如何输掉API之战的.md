Joel on Software

>#How Microsoft Lost the API War

#微软是如何输掉API之战的

>###by Joel Spolsky Sunday, June 13, 2004

---

>Here's a theory you hear a lot these days: "Microsoft is finished. As soon as Linux makes some inroads on the desktop and web applications replace desktop applications, the mighty empire will topple."
有个如今你经常听到的理论：“微软已经完蛋了，一旦Linux开始进军桌面和网络应用程序并且取代桌面应用程序，那么这个强大的帝国就会轰然倒塌”。

>Although there is some truth to the fact that Linux is a huge threat to Microsoft, predictions of the Redmond company's demise are, to say the least, premature. Microsoft has an incredible amount of cash money in the bank and is still incredibly profitable. It has a long way to fall. It could do everything wrong for a decade before it started to be in remote danger, and you never know... they could reinvent themselves as a shaved-ice company at the last minute. So don't be so quick to write them off. In the early 90s everyone thought IBM was completely over: mainframes were history! Back then, Robert X. Cringely predicted that the era of the mainframe would end on January 1, 2000 when all the applications written in COBOL would seize up, and rather than fix those applications, for which, allegedly, the source code had long since been lost, everybody would rewrite those applications for client-server platforms.

虽然Linux是微软最大的威胁这件事情是不争的事实。但是，据此就预言说这个Redmond的公司就要这样消亡了，也未免太过早下定论了。微软在银行里有的大量的现金存款，并且微软仍然保持难以置信的盈利。它要一段很长的一段路才能走向衰落，微软可以保持十年一直做错误的决定，然后才开始面临着远方的危机。并且你永远没法预测，他们永远可以在最后一刻将自己打造成滨光闪亮的新面目。所以请不要这么快把它们划掉。早在九十年代的时候，每个人都觉得IBM已经玩完了，主机系统已经成为历史了。在那个时候，Robert X 神秘的预言道：主机系统将在2000年1月1号终结，那个时候所有用COLBOL写的程序都会停止运行。他宣称源代码早就已经丢失了，所以相比于要修复这些应用程序。他觉得人们应该采用客户端服务器平台重写这些应用程序。

>Well, guess what. Mainframes are still with us,  nothing happened on January 1, 2000, and IBM reinvented itself as a big ol' technology consulting company that also happens to make cheap plastic telephones. So extrapolating from a few data points to the theory that Microsoft is finished is really quite a severe exaggeration.
猜猜怎么着？主机系统仍然还在使用。2000年1月1号什么事情都没有发生。IBM将自己重新打造成了一个技术顾问公司巨头。这家公司碰巧也会生产便宜的塑料电话而已。根据这个理论的一些数据特征可以推断：宣称微软已经完蛋了实在是严重夸大事实了。

>However, there is a less understood phenomenon which is going largely unnoticed: Microsoft's crown strategic jewel, the Windows API, is lost. The cornerstone of Microsoft's monopoly power and incredibly profitable Windows and Office franchises, which account for virtually all of Microsoft's income and covers up a huge array of unprofitable or marginally profitable product lines, the Windows API  is no longer of much interest to developers. The goose that lays the golden eggs is not quite dead, but it does have a terminal disease, one that nobody noticed yet.
然而却有一个不为人知的现象：微软已经丢掉了它的战略皇冠上的宝石。Windows Api。微软独裁力量的基石在于盈利的office品牌，这个品牌几乎占据了微软所有的主要收入，并且掩盖了大量的亏损，或者只是轻微盈利的产品线。程序员不再感兴趣Windows编程借口了。那个下金蛋的鹅没有死，但是它已经得上了一种高危疾病，只是没有人注意到这一点。

>Now that I've said that, allow me to apologize for the grandiloquence and pomposity of that preceding paragraph. I think I'm starting to sound like those editorial writers in the trade rags who go on and on about Microsoft's strategic asset, the Windows API. It's going to take me a few pages, here, to explain what I'm really talking about and justify my arguments. Please don't jump to any conclusions until I explain what I'm talking about. This will be a long article. I need to explain what the Windows API is; I need to demonstrate why it's the most important strategic asset to Microsoft; I need to explain how it was lost and what the implications of that are in the long term. And because I'm talking about big trends, I need to exaggerate and generalize.
既然我已经这样说了，首先请允许我对前一个段落的那种豪言壮语和浮夸的措辞道歉。我觉得我开始有点像那种只会讨论微软战略资产不入流的编剧作家了。要让我讲清楚我的观点和论据可能要花上几页，所以在我讲清楚讨论内容之前请不要轻易地得出任何结论。这是一篇很长的文章，我想我需要解释什么是windows API？为什么它对于微软来说是最重要的战略资产？我需要解释为什么微软已经失去了这个战略资产？以及长远来说意味着什么？而且因为我讨论的都是大的趋势，我可能需要夸张和简化手法。

>Developers, Developers, Developers, Developers
开发人员，开发人员。开发人员。开发人员。

>Remember the definition of an operating system? It's the thing that manages a computer's resources so that application programs can run. People don't really care much about operating systems; they care about those application programs that the operating system makes possible. Word Processors. Instant Messaging. Email. Accounts Payable. Web sites with pictures of Paris Hilton. By itself, an operating system is not that useful. People buy operating systems because of the useful applications that run on it. And therefore the most useful operating system is the one that has the most useful applications.

还记得操作系统的定义吗？操作系统就是管理计算机的资源以便应用程序能够运行的那个东西。人们其实并不是很关心操作系统，他们关心操作系统上启动的应用程序：文字处理器，及时通讯，电子邮件，支付账单，有帕里斯希尔顿照片的网络站点。就其本身而言操作系统并不是很有用。人们之所以会购买操作系统是因为操作系统上面能够运行各种有用的应用程序。因此最有用的操作系统就是有着最有用的应用程序的那一个。

>The logical conclusion of this is that if you're trying to sell operating systems, the most important thing to do is make software developers want to develop software for your operating system. That's why Steve Ballmer was jumping around the stage shouting "Developers, developers, developers, developers." It's so important for Microsoft that the only reason they don't outright give away development tools for Windows is because they don't want to inadvertently cut off the oxygen to competitive development tools vendors (well, those that are left) because having a variety of development tools available for their platform makes it that much more attractive to developers. But they really want to give away the development tools. Through theirEmpower ISV program you can get five complete sets of MSDN Universal (otherwise known as "basically every Microsoft product except Flight Simulator") for about $375. Command line compilers for the .NET languages are included with the free .NET runtime... also free. The C++ compiler is now free. Anything to encourage developers to build for the .NET platform, and holding just short of wiping out companies like Borland.
这段话的逻辑结论就是：如果你要尝试销售操作系统，最重要的事情就是要使得软件开发人员愿意为你的操作系统开发软件。这就是为什么史蒂夫鲍尔默在舞台上跳来跳去，咆哮着：开发者！开发者！开发者!开发者!的原因。开发者对微软是如此重要。他们不公然放弃windows开发工具原因就是在于他们不想在不经意间割断那些有竞争的开发工具提供商的输氧管（那些提供商已经离开了）。因为一旦他们的平台有着多样的开发工具，对于开发者来讲就有吸引力多了。但是他们也真的很想放弃开发工具，通过他们的ISV授权计划,你可以花大概375美元购买完整的MSDN全球版（以包含了基本上微软模拟飞行器之外的所有软件产品著称）；.NET语言命令行编译器也被包含在免费的.NET运行时环境里面；C++编译器现在也是免费的；以及任何鼓励开发者们在.NET的平台上开发的工具。做空并且消灭掉其他的工具提供商，比如Borland公司。

>Why Apple and Sun Can't Sell Computers
为什么苹果公司和SUN公司不能卖电脑。

>Well, of course, that's a little bit silly: of course Apple and Sun can sell computers, but not to the two most lucrative markets for computers, namely, the corporate desktop and the home computer. Apple is still down there in the very low single digits of market share and the only people with Suns on their desktops are at Sun. (Please understand that I'm talking about large trends here, and therefore when I say things like "nobody" I really mean "fewer than 10,000,000 people," and so on and so forth.)
额，当然，听起来有点蠢。苹果公司和SUN公司当然可以卖电脑。但是却不是在两大最赚钱的市场上（也就是企业桌面市场和家用电脑市场）苹果还是远远的排在列表下面占据个位数的市场份额。而那些支持sun公司桌面系统的人则只存在SUN公司。（今天我在讨论大的趋势，当我说到没有这个字眼儿的时候，我的意思其实是少于一千万个人，或者之类的）

>Why? Because Apple and Sun computers don't run Windows programs, or, if they do, it's in some kind of expensive emulation mode that doesn't work so great. Remember, people buy computers for the applications that they run, and there's so much more great desktop software available for Windows than Mac that it's very hard to be a Mac user.
为什么呢？因为苹果和SUN的电脑不能运行windows程序，或者即便是支持的话也是运行在某种特殊的模式下。那种模式下，程序不能高效地运行。请记住，人们购买电脑只是为了能够运行他们需要的应用。而比起Mac来说。Windows系统上面有着多的多的很棒的软件应用。因此，人们很难选择成为一个mac用户。

>Sidebar What is this "API" thing?
侧栏：什么是api？

>If you're writing a program, say, a word processor, and you want to display a menu, or write a file, you have to ask the operating system to do it for you, using a very specific set of function calls which are different on every operating system. These function calls are called the API: it's the interface that an operating system, like Windows, provides to application developers, like the programmers building word processors and spreadsheets and whatnot. It's a set of thousands and thousands of detailed and fussy functions and subroutines that programmers can use, which cause the operating system to do interesting things like display a menu, read and write files, and more esoteric things like find out how to spell out a given date in Serbian, or extremely complex things like display a web page in a window. If your program uses the API calls for Windows, it's not going to work on Linux, which has different API calls. Sometimes they do approximately the same thing. That's one important reason Windows software doesn't run on Linux. If you wanted to get a Windows program to run under Linux, you'd have toreimplement the entire Windows API, which consists of thousands of complicated functions: this is almost as much work as implementing Windows itself, something which took Microsoft thousands of person-years. And if you make one tiny mistake or leave out one function that an application needs, that application will crash.

如果你在编写一个程序，比如说：文字处理器。那么你想要显示一个菜单，或者写一个文件。你得通过使用一些特定的函数调用让操作系统来帮你做这件事情。这些函数调用在不同的操作系统上各不相同。这些函数调用被称作api，它是一个操作系统提供给应用程序开发人员的编程接口。就像Windows提供给那些搭建字处理器和电子表单之类程序的开发人员的是一个大概有上百万个详细而又模糊的函数组成的集合。程序员可以通过这些函数让操作系统做一些有意思的事情，比如说显示一个菜单，读取或写入文件，或者更极端一些事情，比如说用西伯利亚语拼写一个给定的日期，或者极端极端的事情：在一个窗口里面显示一个网页。如果你的应用程序使用了一百个这样的API调用。那么你的程序在Linux里面是无法正常工作的，因为Linux有着不同的api调用（当然有时碰巧他们也会有相同的API）。这就是什么Windows程序不能在Linux下面运行的主要原因。如果你想要让windows程序运行在linux下面，你要么选择重新实现Windows Api。这个集合包含了上百万非常复杂的函数。几乎就等同于重新实现windows自身。而这件事情微软花费了成千上百的人年。并且，那怕你弄错一个或者漏掉了一个程序需要的函数你的应用程序就会崩溃。

>And that's why the Windows API is such an important asset to Microsoft.
这就是为什么WindowsAPI对于微软是非常重要的资产。

>(I know, I know, at this point the 2.3% of the world that uses Macintoshes are warming up their email programs to send me a scathing letter about how much they love their Macs. Once again, I'm speaking in large trends and generalizing, so don't waste your time. I know you love your Mac. I know it runs everything you need. I love you, you're a Pepper, but you're only 2.3% of the world, so this article isn't about you.)
我知道，我知道，到现在为止世界上已经有2.3%的人使用Mac，他们正在启动他们的电子邮件程序给我发一封刻薄的邮件讨论他们是如何如何喜爱他们的MAC电脑。 再次强调，我讨论的是大的趋势，用了泛化方法。所以不要浪费时间，我知道你很爱很爱你们的MAC，我知道她能够运行所有你需要的程序。我爱你，你们就像辣椒一样，但是你只是世界的2.3%。所以这篇文章不是是为你写的。

>The Two Forces at Microsoft
微软的两股力量。

>There are two opposing forces inside Microsoft, which I will refer to, somewhat tongue-in-cheek, as The Raymond Chen Camp and The MSDN Magazine Camp.
在微软内部有着两股相反的力量。我会叫做（叫起来有点而舌头顶脸）陈瑞蒙帮和MSDN杂志帮。

>Raymond Chen is a developer on the Windows team at Microsoft. He's been there since 1992, and his weblog The Old New Thing is chock-full of detailed technical stories about why certain things are the way they are in Windows, even silly things, which turn out to have very good reasons.
陈瑞蒙是微软windows核心团队的一名开发人员，早在1992年的时候他就已经加入了公司。他的网络博客旧的新东西包含了大量的描写细致的技术故事。通常是讨论为什么windows系统里的某些事情是他们现在这个样子，结果哪怕是很傻的事情背后都有着一个很合理的原因。

>The most impressive things to read on Raymond's weblog are thestories of the incredible efforts the Windows team has made over the years to support backwards compatibility:
读瑞蒙的博客最被打动的事情就是Windows系统团队花了难以想像的代价来支持前向兼容的那些故事。

>Look at the scenario from the customer's standpoint. You bought programs X, Y and Z. You then upgraded to Windows XP. Your computer now crashes randomly, and program Z doesn't work at all. You're going to tell your friends, "Don't upgrade to Windows XP. It crashes randomly, and it's not compatible with program Z." Are you going to debug your system to determine that program X is causing the crashes, and that program Z doesn't work because it is using undocumented window messages? Of course not. You're going to return the Windows XP box for a refund. (You bought programs X, Y, and Z some months ago. The 30-day return policy no longer applies to them. The only thing you can return is Windows XP.)

站在客户的角度来看看这个例子：你购买了程序X Y和Z然后把操作系统升级到了WindowsXP，你的电脑开始随机的崩溃。程序根本没办法运行。你会把这个告诉你的朋友们，告诉他们不要升级到WindowsXP，因为这个系统会随机地崩溃。并且和程序Z不兼容。你会去调试的系统来确定是X造成了崩溃，程序没办法运行是因为它使用了没有正式文档的窗口消息么？当然不会，你只会拿着WindowsXP的CD盒要求退退款。你在几个月之前购买的X Y Z 30天退款的条款已经不适用于这些程序。唯一能够退的就是WindowsXP。

>I first heard about this from one of the developers of the hit game SimCity, who told me that there was a critical bug in his application: it used memory right after freeing it, a major no-no that happened to work OK on DOS but would not work under Windows where memory that is freed is likely to be snatched up by another running application right away. The testers on the Windows team were going through various popular applications, testing them to make sure they worked OK, but SimCity kept crashing. They reported this to the Windows developers, who disassembled SimCity, stepped through it in a debugger, found the bug, and added special code that checked if SimCity was running, and if it did, ran the memory allocator in a special mode in which you could still use memory after freeing it.

我第一次是从一个叫做罪恶都市的射击游戏的开发组那里听来这个故事的。他们的应用程序里面有一个重大错误，在释放内存之后马上又使用了这块内存，这个重大的错误碰巧在DOS上面能够运行， 而在Windows系统上面，因为被释放的应用程序内存很有可能又会被另外一个应用程序马上占用。Windows系统团队的测试人员正在测试所有这些流行的应用。他们的主要工作就是测试这些应用程序确保他们能够继续运行，但是罪恶都市却无法运行，于是他们报告给了windows开发团队。开发团队反编译了罪恶都市，采用调试器一步一步调试找到了这个错误，并且加入了一段特殊代码来检查罪恶都市是否在运行，如果确实是在运行，那么他就将内存分配器以一种特殊模式启动，在这种情况下就仍然可以使用释放后的内存。

>This was not an unusual case. The Windows testing team is huge and one of their most important responsibilities is guaranteeing that everyone can safely upgrade their operating system, no matter what applications they have installed, and those applications will continue to run, even if those applications do bad things or use undocumented functions or rely on buggy behavior that happens to be buggy in Windows n but is no longer buggy in Windows n+1. In fact if you poke around in the AppCompatibility section of your registry you'll see a whole list of applications that Windows treats specially, emulating various old bugs and quirky behaviors so they'll continue to work. Raymond Chen writes, "I get particularly furious when people accuse Microsoft of maliciously breaking applications during OS upgrades. If any application failed to run on Windows 95, I took it as a personal failure. I spent many sleepless nights fixing bugs in third-party programs just so they could keep running on Windows 95."
这是一个非比寻常的案例。Windows系统测试团队最重要的职责就是保证每一个人都能安全的升级操作系统。不管他们安装了什么应用程序，那些应用程序都要能够继续运行。哪怕这些应用程序做了很糟糕的事情：使用了没有正式文档的技术；或者他们碰巧利用了Windows N的一个错误，而这个错误在Windows N+1里已经被修复了。 如果你在你的注册表里面的应用程序兼容性部分随便看看的话，你就会发现整整一个列表的特殊应用程序，为了让这些程序能够继续运行，Windows特别模拟了各种旧的错误，奇怪的行为,只为了让这些应用程序能够继续工作。陈瑞蒙这样写道：当人们指责微软在系统升级的时候恶意地打破应用程序的运行，我都会发怒。 如果任何应用程序不能够在windows95上运行，我都会将其看成一个个人失败。我花费了无数不眠之夜为第三方应用程序修复错误只是为了保证他们能够继续在windows95系统就上面运行。

>A lot of developers and engineers don't agree with this way of working. If the application did something bad, or relied on some undocumented behavior, they think, it should just break when the OS gets upgraded. The developers of the Macintosh OS at Apple have always been in this camp. It's why so few applications from the early days of the Macintosh still work. For example, a lot of developers used to try to make their Macintosh applications run faster by copying pointers out of the jump table and calling them directly instead of using the interrupt feature of the processor like they were supposed to. Even though somewhere in Inside Macintosh, Apple's official Bible of Macintosh programming, there was a tech note saying "you can't do this," they did it, and it worked, and their programs ran faster... until the next version of the OS came out and they didn't run at all. If the company that made the application went out of business (and most of them did), well, tough luck, bubby.
有许多开发者和工程师并不同意这种工作方式。如果程序做错什么样事情，或者依赖于一些没有被正式文档的行为，他们觉得在操作系统升级的时候，这些程序就是应该失效。MAC操作系统的开发者就是这个阵营的支持者。这也是为什么很少有早期mac上的程序到现在还能运行的原因。比方说，很多开发者经常通过这样的方式让他们的mac应用程序运行得更快，他们会把指针从跳表里面拷贝出来，然后直接通过指针调用。而不是按照建议的方式去使用处理器的中断特性，虽然在苹果的编程指南圣经“Mactonish内部指南”里面有名明确的有一条记载着说你不能这样做，他们还是去这样做并且也能工作，而且这样他们的程序运行得更快。直到下一个版本的操作系统出来的时候他们的程序就不能够继续运行了。如果编写这个应用程序的公司最终破产了(实际上大部分确实不上了)额。兄弟,你太不走运了。

>To contrast, I've got DOS applications that I wrote in 1983 for the very original IBM PC that still run flawlessly, thanks to the Raymond Chen Camp at Microsoft. I know, it's not just Raymond, of course: it's the whole modus operandi of the core Windows API team. But Raymond has publicized it the most through his excellent website The Old New Thing so I'll name it after him.
相比之下，我就可以拿出在1983年的时候为最初的IBMPC编写的DOS程序，这个程序仍然能够不错的继续运行。多亏了这位人的陈瑞萌。我知道当然不仅仅是陈瑞萌。多亏了WindowsApi核心的团队这种处理方法。但是陈瑞萌最先公开了这些故事，所以我将这个阵营以他命名。

>That's one camp. The other camp is what I'm going to call the MSDN Magazine camp, which I will name after the developer's magazine full of exciting articles about all the different ways you can shoot yourself in the foot by using esoteric combinations of Microsoft products in your own software. The MSDN Magazine Camp is always trying to convince you to use new and complicated external technology like COM+, MSMQ, MSDE, Microsoft Office, Internet Explorer and its components, MSXML, DirectX (the very latest version, please), Windows Media Player, and Sharepoint... Sharepoint! which nobodyhas; a veritable panoply of external dependencies each one of which is going to be a huge headache when you ship your application to a paying customer and it doesn't work right. The technical name for this is DLL Hell. It works here: why doesn't it work there?
这只是一个阵营，另外一个阵营我常常叫做MSDN杂志阵营。这个阵营我以开发者杂志命名。这个杂志充满了令人激动的文章，全部都是关于讨论如何通过在你自己的软件里面采用各种深奥的微软产品的组合来砸到自己的脚。MSDN杂志阵营总是尝试着说服你去采用最复杂的技术。例如：COM+, MSMQ, MSDE, 微软Office, Internet Explorer 及其组件： MSXML, DirectX (拜托请用最新版本), Windows媒体播放器, 和Sharepoint等等。 咦？SharePoint？没人有Sharepoint啊？等一系列真正的全副武装的外部依赖。当你要把你的应用程序发布给一个付钱的客户的时候，VB不能够正确地工作。每一个这种外部一代都能成为巨大头疼问题。技术上来讲，这通常又叫Dll 地狱。在我这里是能工作的，为什么到了你那里就不能工作呢？

>The Raymond Chen Camp believes in making things easy for developers by making it easy to write once and run anywhere (well, on any Windows box). The MSDN Magazine Camp believes in making things easy for developers by giving them really powerful chunks of code which they can leverage, if they are willing to pay the price of incredibly complicated deployment and installation headaches, not to mention the huge learning curve. The Raymond Chen camp is all about consolidation. Please, don't make things any worse, let's just keep making what we already have still work. The MSDN Magazine Camp needs to keep churning out new gigantic pieces of technology that nobody can keep up with.

陈瑞蒙的阵营相信一次编写随处运行（当然是指windows系统机器）更容易让开发者的生活变得更轻松。MSDN杂志阵营则相信通过给予开发者们能够御用的非常强大的代码组件使程序员的生活更加轻松。当然，你首先要愿意付出极度复杂的部署和安装代价（巨大的学习曲线困难之类的代价更不用提了）。陈瑞蒙阵营关心的是整合，拜托！不要让事情变得更糟了。保持让所有的东西继续正常运作。而MSDN阵营只需要保证产出巨大的新技术，没有人能够跟上的新技术。

>Here's why this matters.
以下就是重点？

>Microsoft Lost the Backwards Compatibility Religion
微软已经失去了前向兼容性的信仰。

>Inside Microsoft, the MSDN Magazine Camp has won the battle.
在微软内部MSDN杂志阵营已经取得了胜利。

>The first big win was making Visual Basic.NET not backwards-compatible with VB 6.0. This was literally the first time in living memory that when you bought an upgrade to a Microsoft product, your old data (i.e. the code you had written in VB6) could not be imported perfectly and silently. It was the first time a Microsoft upgrade did not respect the work that users did using the previous version of a product.
第一巨大的胜利就是使得VISUAL BASIC.NET不再兼容VB6.0。这是我记忆中第一次，你购买微软产品的一个升级包，然后发现你的一些旧的数据（你用vb6编写的代码）不能够被静静地完美地导入。微软公司的产品升级包没有尊重用户使用该产品的前一版本产生的工作。

>And the sky didn't seem to fall, not inside Microsoft. VB6 developers were up in arms, but they were disappearing anyway, because most of them were corporate developers who were migrating to web development anyway. The real long term damage was hidden.
天好像也没有塌下来。至少在微软内部没有。不管怎样。VB6.0开发者曾经揭竿而起，但还是消失了。因为他们中的大多数也只是企业应用开发者，他们总归也会迁移到网页开发。而真正的长期伤害却被隐藏起来。

>With this major victory under their belts, the MSDN Magazine Camp took over. Suddenly it was OK to change things. IIS 6.0 came out with a different threading model that broke some old applications. I was shocked to discover that our customers with Windows Server 2003 were having trouble running FogBugz. Then .NET 1.1 was not perfectly backwards compatible with 1.0. And now that the cat was out of the bag, the OS team got into the spirit and decided that instead of adding features to the Windows API, they were going to completely replace it. Instead of Win32, we are told, we should now start getting ready forWinFX: the next generation Windows API. All different. Based on .NET with managed code. XAML. Avalon. Yes, vastly superior to Win32, I admit it. But not an upgrade: a break with the past.

这场重大胜利之后，MSDN杂志阵营取得了完全胜利。突然可以改变任何东西了：IIS6.0提出了一种打破一些旧应用程序运行方式的线程模型。我震惊地发现升级到windows服务器版本2003的时候，客户在运行FOGBUGZ的时候遇到了麻烦；然后NET1.1没有完全兼容1.0；然后到现在，猫已经从袋子里面爬了出来。操作系统团队得到了这种精神要领，然后决定相比于向现有的windows api增加功能，他们要完全取代这些功能。我们被告知我们现在应该要准备好迎接下一代的windows api接口WINFX，而不是WIN32。WINFX 基于.NET 托管代码采用XAML Avalon比WIN32好多了。是的我承认。但是却不能称为是升级，因为打破了过去。

>Outside developers, who were never particularly happy with the complexity of Windows development, have defected from the Microsoft platform en-masse and are now developing for the web. Paul Graham, who created Yahoo! Stores in the early days of the dotcom boom, summarized it eloquently: "There is all the more reason for startups to write Web-based software now, because writing desktop software has become a lot less fun. If you want to write desktop software now you do it on Microsoft's terms, calling their APIs and working around their buggy OS. And if you manage to write something that takes off, you may find that you were merely doing market research for Microsoft."

外界的那些程序员从来就没有对windows程序开发的复杂度特别满意，现在更是开始大批的撤离微软平台，然后开始进行网络应用开发。Paul Graham （就是那个在.COM泡沫早起时代创建雅虎商店的那个家伙）雄辩地总结道：现在为什么初创公司应该要选择面向网页的软件开发有有更多的理由了，因为开发桌面软件已经变得更加无趣了。如果你要开发桌面软件，你得用微软的方式，要用他们充满错误的操作系统。并且如果你最终设法写出了一些能够卖座的东西。你会发现你不过是在为微软做市场调研罢了。

>Microsoft got big enough, with too many developers, and they were too addicted to upgrade revenues, so they suddenly decided that reinventing everything was not too big a project. Heck, we can do it twice. The old Microsoft, the Microsoft of Raymond Chen, might have implemented things like Avalon, the new graphics system, as a series of DLLs that can run on any version of Windows and which could be bundled with applications that need them. There's no technical reason not to do this. But Microsoft needs to give you a reason to buy Longhorn, and what they're trying to pull off is a sea change, similar to the sea change that occurred when Windows replaced DOS. The trouble is that Longhorn is not a very big advance over Windows XP; not nearly as big as Windows was over DOS. It probably won't be compelling enough to get people to buy all new computers and applications like they did for Windows. Well, maybe it will, Microsoft certainly needs it to be, but what I've seen so far is not very convincing. A lot of the bets Microsoft made are the wrong ones. For example, WinFS, advertised as a way to make searching work by making the file system be a relational database, ignores the fact that the real way to make searching work is by making searching work.Don't make me type metadata for all my files that I can search using a query language. Just do me a favor and search the damned hard drive, quickly, for the string I typed, using full-text indexes and other technologies that were boring in 1973.
微软已经成长地足够大了，它拥有太多的程序员。这些程序员已经沉醉于升级带来的收入了。于是他们突然发现重新发明了一样东西也不是那么大的一个项目。滚，我们都可以做两遍了。那些老微软人，比如微软的陈瑞蒙可能会说：我们会实现一些像Avalon一样的东西，一种新的图形系统。这个图形可以通过运行在任何版本的windows上的。可以以Dll库的形式提供给需要的用户，和那些需要它们的应用程序一起打包。没有任何技术的原因说明不能这样做。但是需要一个理由说服你尝试购买longhorn。他们要推进的是像大海那样的改动，跟当年微软决定从DOS改动到WINDOWS那样大的改动。问题在于：LONGHORN相比于XP并没有提供太多的改进之处，并不像windows取代DOS那样有足够的说服力，让人们（像当初从DOS迁移到WINDOWS那样）去购买新的电脑和新应用程序，额，也许也会。微软当然需要那样，但是目前为止我所看到的并不能令人信服。微软打的很多赌都错了，比如说：WINFS正如广告宣传的那样，通过把文件系统做成关系数据库，来加快搜索速度。但是这样做忽略了这样一个事实：就是真正要让搜索变快，只需要让搜索变快而已！ 我不需要什么类型元信息，不要说给我所有文件加上类型元信息就可以进行快速搜索了。只要采用全文索引或者其他在1973年发明的某项无聊技术对于我输入的查询字符串帮我快速的搜索硬盘就可以了。

>Automatic Transmissions Win the Day

自动变速赢得了这一天的胜利。

>Don't get me wrong... I think .NET is a great development environment and Avalon with XAML is a tremendous advance over the old way of writing GUI apps for Windows. The biggest advantage of .NET is the fact that it has automatic memory management.

不要理解错了，我觉得.NET是很棒的开发环境，附带XAML的Avalon相比在旧的windows系统上面开发用户界面程序也是巨大的进步，但是.NET最大的优势在于自动内存管理。

>A lot of us thought in the 1990s that the big battle would be between procedural and object oriented programming, and we thought that object oriented programming would provide a big boost in programmer productivity. I thought that, too. Some people still think that. It turns out we were wrong. Object oriented programming is handy dandy, but it's not really the productivity booster that was promised. The realsignificant productivity advance we've had in programming has been from languages which manage memory for you automatically. It can be with reference counting or garbage collection; it can be Java, Lisp, Visual Basic (even 1.0), Smalltalk, or any of a number of scripting languages. If your programming language allows you to grab a chunk of memory without thinking about how it's going to be released when you're done with it, you're using a managed-memory language, and you are going to be much more efficient than someone using a language in which you have to explicitly manage memory. Whenever you hear someone bragging about how productive their language is, they're probably getting most of that productivity from the automated memory management, even if they misattribute it.
我们中很多人都觉得九十年代最大的战役肯定是发生在面向过程和面向对象编程语言之间。并且我们当时觉得面向对象的编程语言会给程序员的生产效率带来巨大的提升，我也那样觉得，仍然有一些人这样觉得。结果证明我们是错的。面向对象编程不过是些奇技淫巧，并没有像承诺的那样真正的提升了生产效率。真正获得的生产效率提升来自于那些为你提供自动内存管理的语言，可以是引用计数或者是垃圾回收，可以是Java, Lisp, Visual Basic (甚至1.0), Smalltalk,或者其他任何相当的脚本语言。如果使用的编程语言可以让你随便拿一块内存，不需要考虑如何释放这款内存。当你用完这款内存的时候托管内存会自动释放，在这种情况下你就会比那些采用显式内存管理的人来得有效率得多。不管什么时候当你听说，他们采用的语言是多么的有效率，他们获得的大部分效率也许就来自自动内存管理，哪怕他们自己都归错了功劳。

>####Sidebar

####侧栏
>Why does automatic memory management make you so much more productive? 1) Because you can writef(g(x)) without worrying about how to free the return value from g, which means you can use functions which return interesting complex data types and functions which transform interesting complex data types, in turn allowing you to work at a higher level of abstraction. 2) Because you don't have to spend any time writing code to free memory or tracking down memory leaks. 3) Because you don't have to carefully coordinate the exit points from your functions to make sure things are cleaned up properly.
为什么自动内存管理会让你变得更有效率呢？1 因为你可以编写这样的函数调用f(g(x))而不需要考虑g函数的返回值如何释放。 这就意味着你可以使用函数返回一些有趣的复杂的数据类型。你可以使用函数来变换一些复杂的数据类型。继而允许你在一个更高层次的抽象级别上工作。 2 因为你不需要写代码释放内存或者追踪内存泄漏。 3 因为你不需要仔细的协调函数的退出点来保证所有的资源的正确释放。

>Racing car aficionados will probably send me hate mail for this, but my experience has been that there is only one case, in normal driving, where a good automatic transmission is inferior to a manual transmission. Similarly in software development: in almost every case, automatic memory management is superior to manual memory management and results in far greater programmer productivity.
赛车的粉们可能会向我发来怒骂的邮件。但是根据我的经验：在正常的驾驶状况下，只有极个别情况，好的自动变速车会次于手动变速车。同样的软件开发领域，几乎在每一个情况下自动内存管理都要比手动的内存管理优越并且进而使程序员生产力效率更高。

>If you were developing desktop applications in the early years of Windows, Microsoft offered you two ways to do it: writing C code which calls the Windows API directly and managing your own memory, or using Visual Basic and getting your memory managed for you. These are the two development environments I have used the most, personally, over the last 13 years or so, and I know them inside-out, and my experience has been that Visual Basic is significantly more productive. Often I've written the same code, once in C++ calling the Windows API and once in Visual Basic, and C++ always took three or four times as much work. Why? Memory management. The easiest way to see why is to look at the documentation for any Windows API function that needs to return a string. Look closely at how much discussion there is around the concept of who allocates the memory for the string, and how you negotiate how much memory will be needed. Typically, you have to call the function twice—on the first call, you tell it that you've allocated zero bytes, and it fails with a "not enough memory allocated" message and conveniently also tells you how much memory you need to allocate. That's if you're lucky enough not to be calling a function which returns a list of strings or a whole variable-length structure. In any case, simple operations like opening a file, writing a string, and closing it using the raw Windows API can take a page of code. In Visual Basic similar operations can take three lines.

如果早年的时候你在windows系统上开发过桌面应用程序，微软给你提供了两种方式来达成这一目标。你可以编写C语言代码直接调用windows api，然后自己管理自己的内存。或者使用VisualBasic，这样系统帮你管理内存。这是我过去13年来个人使用过的最主要的两种开发环境。并且我从里到外都很了解这两种技术。我的经验就是VisualBasic要高效的多。通常如果我编写相同的代码：一次用C++调用windows系统api；一次用VisualBasic。C++总是要花费3到4倍的时间，为什么呢？内存管理。了解为什么最容易的方式就是去随便看看任何关于字符串windows系统api函数的文档。仔细的了解是谁分配了字符串的内存，以及你如何协商你需要多大的内存。通常你需要调用函数两次。第一次调用的时候，你告诉他你已经分配了零字节，然后它就很自然的产生内存不足的失败消息，然后告诉你你需要分配多大内存。这种情况还得是你足够幸运没有牵扯到调用一个返回字符串列表的函数或者是可变长度结构的函数。不管在哪种情况下，想打开文件，写入字符串，关闭文件。采用原始的WindowsAPI做的这些简单工作都能够花上一整页的代码，而在VisualBasic同样的操作可能只需要两三行代码。

>So, you've got these two programming worlds. Everyone has pretty much decided that the world of managed code is far superior to the world of unmanaged code. Visual Basic was (and probably remains) the number one bestselling language product of all time and developers preferred it over C or C++ for Windows development, although the fact that "Basic" was in the name of the product made hardcore programmers shun it even though it was a fairly modern language with a handful of object-oriented features and very little leftover gunk (line numbers and the LET statement having gone the way of the hula hoop). The other problem with VB was that deployment required shipping a VB runtime, which was a big deal for shareware distributed over modems, and, worse, let other programmers see that your application was developed in (the shame!) Visual Basic.
所以你就得到了两个编程世界。每个人大概已经同意了托管代码的世界要比非托管代码的世界优越的多。VisualBasic曾经是（可能仍然是）一直以来排行第一的最畅销的编程语言，比起Windows开发的C/C++语言开发怎么开发者可能更加倾向于VisualBasic。 虽然产品的名字中间有“基础”这样的字眼让老牌的程序员对之嗤之以鼻。即使这样VB也是非常现代的，并且有一些面向对象特性，很少缺点（行号和LET语句已经给呼啦圈LOOP让路了）的一门语言。 VB的其他问题在于：部署的时候需要发布一个VB运行时环境。这个运行时环境对于通过调制解调器部署的共享软件来说是个大问题。更糟的是，这就让其他程序员看到了你的应用程序是使用（太丢脸了）VB开发的。

>One Runtime To Rule Them All

一个运行时环境管所有

>And along came .NET. This was a grand project, the super-duper unifying project to clean up the whole mess once and for all. It would have memory management, of course. It would still have Visual Basic, but it would gain a new language, one which is in spirit virtually the same as Visual Basic but with the C-like syntax of curly braces and semicolons. And best of all, the new Visual Basic/C hybrid would be called Visual C#, so you would not have to tell anyone you were a "Basic" programmer any more. All those horrid Windows functions with their tails and hooks and backwards-compatibility bugs andimpossible-to-figure-out string-returning semantics would be wiped out, replaced by a single clean object oriented interface that only has one kind of string. One runtime to rule them all. It was beautiful. And they pulled it off, technically. .NET is a great programming environment that manages your memory and has a rich, complete, and consistent interface to the operating system and a rich, super complete, and elegant object library for basic operations.
然后。NET就诞生了，这是一个很大的项目。这个超级噱头的，统一化项目致力于一次清理所有的糟糕问题。当然他会有内存管理，还是会有VISUAL BASIC。但是他会获得一种新的语言，一种本质上跟VISUAL BASIC一样，但是却有着c语言语法（大括号和分好）一样的语言。然后最棒的是这种新的VISUAL BASIC/C混合语言被叫做VISUAL C#，这样你就不再告诉任何人，你是一个“基础”程序员。那些所有糟糕的Windows系统函数留下的尾巴，钩子，前向兼容错误以及已经没有办法搞清楚的返回字符串与语义问题都会被一笔擦掉。取而代之的是唯一的干净的面向对象的接口，这种接口只有一种字符串。一个运行时环境解决所有这些问题。这很漂亮。技术上来说把问题解决了，.NET是伟大的编程编程环境它帮你管理内存，丰富完整一致的操作系统的接口，有一套用来进行基本的操作的超级完整的丰富优雅的对象库。

>And yet, people aren't really using .NET much.
然而人们还没有真正开始用.NET

>Oh sure, some of them are.
哦，当然他们中有些人会用的。

>But the idea of unifying the mess of Visual Basic and Windows API programming by creating a completely new, ground-up programming environment with not one, not two, but three languages (or are there four?) is sort of like the idea of getting two quarreling kids to stop arguing by shouting "shut up!" louder than either of them. It only works on TV. In real life when you shout "shut up!" to two people arguing loudly you just create a louder three-way argument.

通过从头开始重新创建一个完全崭新的编程环境来统一解决VISUALBASIC和windows系统api留下的糟糕问题。这个新的环境拥有不是一个，不是两个，而是三种语言（什么？有四个吗？）这种想法就好比是在处理两个小孩儿吵架的局面， 你用一种比他们俩都大声的语调朝他们嚷“闭嘴”。这种情况只有在电视里才行得通。在现实生活中，如果你朝两个争吵的人大声的。嚷道“闭嘴”。你不过是创建了一个声音更大的三方争吵罢了。

>(By the way, for those of you who follow the arcane but politically-charged world of blog syndication feed formats, you can see the same thing happening over there. RSS became fragmented with several different versions, inaccurate specs and lots of political fighting, and the attempt to clean everything up by creating yet another format called Atom has resulted in several different versions of RSS plus one version of Atom, inaccurate specs and lots of political fighting. When you try to unify two opposing forces by creating a third alternative, you just end up with three opposing forces. You haven't unified anything and you haven't really fixed anything.)
（顺带说一下。如果你用过被政治化争论统治的神秘的博客订阅格式，你会发现这里发生着同样的事情。RSS变成了有着不同版本的碎片化的规范不明确格式。一直有很多政治力量的在争论。然后有一种想法想通过创建一种一种新的格式叫做ATOM格式来清理所有这些糟糕问题的。最后导致了若干个不同版本的RSS和一个新的ATOM，仍然是大量的政治争论和不精确的规范。当你想通过创建一个第三方力量来统一两种相反的力量，最后只会获得三种不同的力量。你没有统一任何东西，也没有修复任何东西。）

>So now instead of .NET unifying and simplifying, we have a big 6-way mess, with everybody trying to figure out which development strategy to use and whether they can afford to port their existing applications to .NET.
所以这种局面下.NET没有统一或修复任何东西。我们现在有了一个六方参与的糟糕问题局面。每个人都在尝试搞清楚他们应该采用哪种开发策略，他们是不是能够承担得起将他们现有的应用程序移植到.NET平台。

>No matter how consistent Microsoft is in their marketing message ("just use .NET—trust us!"), most of their customers are still using C, C++, Visual Basic 6.0, and classic ASP, not to mention all the other development tools from other companies. And the ones that are using .NET are using ASP.NET to develop web applications, which run on a Windows server but don't require Windows clients, which is a key point I'll talk about more when I talk about the web.
不管微软在他们的市场营销信息中是如何一致（相信我们！就用.NET!）他们大部分的客户还是在使用C/ C++ 和VB6.0以及经典的ASP ，更不要提其他公司提供的开发工具了。那些采用.NET的人其实也只是在用ASP.NET开发网页应用程序。这些应用程序是运行在windows系统服务器上，但是他们却不需要windows客户端。关于这一点我会在谈到网页的时候重点讨论。

>Oh, Wait, There's More Coming!

哦，等等，还有更多的事情发生了。

>Now Microsoft has so many developers cranking away that it's not enough to reinvent the entire Windows API: they have to reinvent ittwice. At last year's PDC they preannounced the next major version of their operating system, codenamed Longhorn, which will contain, among other things, a completely new user interface API, codenamedAvalon, rebuilt from the ground up to take advantage of modern computers' fast display adapters and realtime 3D rendering. And if you're developing a Windows GUI app today using Microsoft's "official" latest-and-greatest Windows programming environment, WinForms, you're going to have to start over again in two years to support Longhorn and Avalon. Which explains why WinForms is completely stillborn. Hope you haven't invested too much in it. Jon Udell found a slide from Microsoft labelled "How Do I Pick Between Windows Forms and Avalon?" and asks, "Why do I have to pick between Windows Forms and Avalon?" A good question, and one to which he finds no great answer.
好吧，现在微软有如此多的程序员在嚷嚷着重新发明windows系统api是不够的，必须得重新发明两次。去年的PDC大会上他们预先宣布了 代号为LONGHORN的下一个操作系统大版本。这个新版本除了其他东西之外，还有一个代号Avalon的新用户界面api。Avalon采用了现代计算机快速显示能力和实时三维渲染能力从头开始打造。所以如果你打算开发一个windows用户界面应用程序，现在你还得采用微软官方最新最伟大的Windows系统编程环境WINFORMS，但是一两年后你可能得从头开始来过以支持LONGHORN和AVALON。 这解释了为什么WINFORM会胎死腹中，希望你还没有在这项技术上投入太大代价。JonUdell发现了一个微软制作的幻灯片，标题为“在WINFORM和AVALON之间应该如何选择？ 他问道：“我为什么要在WINFORM和AVALON之间进行选择：”好问题，但是他发现这个问题没有很好的答案。

>So you've got the Windows API, you've got VB, and now you've got .NET, in several language flavors, and don't get too attached to any of that, because we're making Avalon, you see, which will only run on the newest Microsoft operating system, which nobody will have for a loooong time. And personally I still haven't had time to learn .NET very deeply, and we haven't ported Fog Creek's two applications from classic ASP and Visual Basic 6.0 to .NET because there's no return on investment for us. None. It's just Fire and Motion as far as I'm concerned: Microsoft would love for me to stop adding new features to our bug tracking software and content management software and instead waste a few months porting it to another programming environment, something which will not benefit a single customer and therefore will not gain us one additional sale, and therefore which is a complete waste of several months, which is great for Microsoft, because they have content management software and bug tracking software, too, so they'd like nothing better than for me to waste time spinning cycles catching up with the flavor du jour, and then waste another year or two doing an Avalon version, too, while they add features to their own competitive software. Riiiight.
所以你可以用windows api，可以用VB，然后现在你还可以用到.NET。并且选择若干不同的语言风格。但是呢，请不要对这些技术对这些技术太过深入因为我们还在开发AVALON。你明白了吗？这项新技术会运行在微软最新的操作系统上。人们已经好久没有新的操作系统了。 就个人而言，我还是没有时间去深入的学习.NET，而且我们还没有把FOGCREEK的两个应用程序从经典的VB6.0和ASP架构移植到.NET平台，因为这件事情对我来讲没有太大的投资回报，根本就没有。在我看来这就是移动开火策略而已： 微软很乐于看到我们停止向我们的错误追踪软件或者是内容管理软件添加新的功能，而是浪费若干个月的时间来把这些软件移植到另外一个编程环境。这件事情根本不会使任何的终端用户受益，因此不会给我们带来任何额外的销售，这完全就是浪费了这几个月。这件事情对于微软来说却是好事，因为他们也有内容管理软件和错误追踪软件，所以如果我浪费一个开发周期来赶上他们的新开发风格的话这对他们来说是再好不过了，然后再浪费个一两年来开发个AVALON版本。与此同时他们却可以向他们的竞争软件添加新的功能。对极了。

>No developer with a day job has time to keep up with all the new development tools coming out of Redmond, if only because there aretoo many dang employees at Microsoft making development tools!

任何有工作的开发者都没有办法有时间来赶上Redmond开发出来的新开发工具的速度，这只是因为微软有太多的员工在开发新的开发工具了。

>It's Not 1990
但这不是1990年。

>Microsoft grew up during the 1980s and 1990s, when the growth in personal computers was so dramatic that every year there were more new computers sold than the entire installed base. That meant that if you made a product that only worked on new computers, within a year or two it could take over the world even if nobody switched to your product. That was one of the reasons Word and Excel displaced WordPerfect and Lotus so thoroughly: Microsoft just waited for the next big wave of hardware upgrades and sold Windows, Word and Excel to corporations buying their next round of desktop computers (in some cases their first round). So in many ways Microsoft never needed to learn how to get an installed base to switch from product N to product N+1. When people get new computers, they're happy to get all the latest Microsoft stuff on the new computer, but they're far less likely to upgrade. This didn't matter when the PC industry was growing like wildfire, but now that the world is saturated with PCs most of which are Just Fine, Thank You, Microsoft is suddenly realizing that it takes much longer for the latest thing to get out there. When they tried to "End Of Life" Windows 98, it turned out there were still so many people using it they had to promise to support that old creaking grandma for a few more years.

微软成长于上世纪八十年代和九十年代。当时，个人计算机的发展是如此的迅速。每年都有超过装机数量的新电脑被卖出。这就意味着即使你的产品在只在新的电脑上运行，那么在一两年内，哪怕没有任何人转向你的新产品，你的产品还是能够统治世界。这就是为什么word和excel从根本上取代了wordperfect和lotus的根本原因。微软只是在等待下一波硬件升级的到来，然后向企业卖出他们的windows，进而为他们的下一轮桌面电脑战略争取时间（某种意义上是他们的第一轮）。所以在很多方面微软从来不需要学习如何去争取那些现有的用户，如何从产品N转移到产品N+1。当人们购买新的计算机的时候，他们很乐于购买微软计算机上面的所有东西，但是他们却远不情愿升级。而这一点在当时并不是很重要，因为当时的pc产业就像野火一般燃烧开来。但是现在的世界已经满足于大部分“还不错”这样的电脑了。不错的能够工作的个人计算机。谢谢你。微软突然意识到要把他们最新的产品发布出去要花比他们想像的多的多的时间。当年他们想要终结windows98生命周期的时候，他们发现外面还是有很多的人在使用，于是他们只好承诺说他们会再为这种操作系统提供多几年的用户支持。

>Unfortunately, these Brave New Strategies, things like .NET and Longhorn and Avalon, trying to create a new API to lock people into, can't work very well if everybody is still using their good-enough computers from 1998. Even if Longhorn ships when it's supposed to, in 2006, which I don't believe for a minute, it will take a couple of years before enough people have it that it's even worth considering as a development platform. Developers, developers, developers, and developers are not buying into Microsoft's multiple-personality-disordered suggestions for how we should develop software.
不幸的是，是这些勇敢的新策略，像.NET LONGHORN和AVALON  尝试创建新的api接口将人们锁定在这个平台上，但是如果人们还在使用着他们1998年购买的，并且觉得足够好的计算机的话，这种战略就无法奏效。那怕LONGHORN在2006年的时候能够按照计划发布（当然我一点都不相信）。在那之后还要花费若干年，人们才会说这个新的操作系统值得被当成是新的开发平台。开发者开发者开发者开发者，他们并没有买微软的帐。他没有听从这个多重人格分裂的家伙向他们提供的关于应该如何开发软件的建议！

>Enter the Web
进入网络时代。

>I'm not sure how I managed to get this far without mentioning the Web. Every developer has a choice to make when they plan a new software application: they can build it for the web or they can build a "rich client" application that runs on PCs. The basic pros and cons are simple: Web applications are easier to deploy, while rich clients offer faster response time enabling much more interesting user interfaces.
我也很诧异在谈及网络之前我就能扯这么远。当每一个程序员策划一个新的软件的时候他们都有一个选择：可以选择开始创建网页应用程序，也可以选择创建运行在个人电脑上的富客户端应用程序。这两者最基本的有点和缺点一目了然：网络应用程序非常容易发布。而富客户端应用程序则拥有更快响应时间和更加有趣的用户界面。

>Web Applications are easier to deploy because there's no installation involved. Installing a web application means typing a URL in the address bar. Today I installed Google's new email application by typing Alt+D, gmail, Ctrl+Enter. There are far fewer compatibility problems and problems coexisting with other software. Every user of your product is using the same version so you never have to support a mix of old versions. You can use any programming environment you want because you only have to get it up and running on your own server. Your application is automatically available at virtually every reasonable computer on the planet. Your customers' data, too, is automatically available at virtually every reasonable computer on the planet.
网络应用程序更容易部署是因为他们不需要安装。安装一个网络应用程序意味着你只需要在地址栏里面插入一个url。今天我刚刚安装了google的新email程序，安装过程就是敲入：Alt+D, gmail, Ctrl+Enter。 网络应用程序没有和其他应用软件的兼容性问题。产品的所有用户都使用都使用同一个版本，你根本不需要支持一堆旧的版本。你可以选择任何你喜欢的编程环境，只需要把它搭起来然后运行在你自己的服务器上面。在这之后几乎能够在地球上任何一个正常的计算机上面使用起来；顾客的数据同样自动的能在地球上每一个正常的计算机上都能够获取到。
---

>But there's a price to pay in the smoothness of the user interface. Here are a few examples of things you can't really do well in a web application:

>  1 .	Create a fast drawing program

>  2 .	Build a real-time spell checker with wavy red underlines
>  3 .	Warn users that they are going to lose their work if they hit the close box of the browser

>  4 .	Update a small part of the display based on a change that the user makes without a full roundtrip to the server

>  5 .	Create a fast keyboard-driven interface that doesn't require the mouse
>  6 .	Let people continue working when they are not connected to the Internet

---

代价就是用户界面的顺畅性，下面就是几个采用网页应用程序没办法做好的例子。

>  1 创建快速的绘图程序。

>  2 创建一个实时的会红色下划线的拼写检查器。

>  3 当用户点击浏览器的关闭按钮的时候，警告用户说他们会丢失他们当前的工作。

>  4 根据用户所做的修改，在不和服务器完成发生一次完整通信的情况下，进行一小部分的显示更新。

>  5 在没有连接到因特网的情况下，让人们继续工作。

---

>These are not all big issues. Some of them will be solved very soon by witty Javascript developers. Two new web applications, Gmail andOddpost, both email apps, do a really decent job of working around or completely solving some of these issues. And users don't seem to care about the little UI glitches and slowness of web interfaces. Almost all the normal people I know are perfectly happy with web-based email, for some reason, no matter how much I try to convince them that the rich client is, uh, richer.
这些都不是什么大问题，其中的一些很快就会被那些聪明的JavaScript开发人员解决掉。例如：两个新的网页应用程序，GMAIL和ODDPOST，都是电子邮件应用程序都采取其他措施完整的解决了上面提到的几个问题，这方面确实做得不错。并且用户看起来似乎也不在乎那些微小的界面问题 或者是网络应用程序的轻微缓慢现象。我认识的几乎所有人完全能接受基于网页的电子邮件，不管我如何尝试说服他们富客户端有更丰富的特性。

>So the Web user interface is about 80% there, and even without new web browsers we can probably get 95% there. This is Good Enough for most people and it's certainly good enough for developers, who have voted to develop almost every significant new application as a web application.
所以网页用户接口已经完成了80%，哪怕没有新的网页浏览器，我大概也能够做到95%。对大多数人来讲就已经足够好了。对于开发者来讲到这更是足够好了。在投票决定每一个重要应用程序应该用什么技术来开发的时候，大多数的开发人员都会投票给网页应用。


>Which means, suddenly, Microsoft's API doesn't matter so much. Web applications don't require Windows.

就意味着微软的api不那么重要了，网页应用程序并不要求必须是windows系统。

>It's not that Microsoft didn't notice this was happening. Of course they did, and when the implications became clear, they slammed on the brakes. Promising new technologies like HTAs and DHTML were stopped in their tracks. The Internet Explorer team seems to have disappeared; they have been completely missing in action for several years. There's no way Microsoft is going to allow DHTML to get any better than it already is: it's just too dangerous to their core business, the rich client. The big meme at Microsoft these days is: "Microsoft is betting the company on the rich client." You'll see that somewhere in every slide presentation about Longhorn. Joe Beda, from the Avalon team, says that "Avalon, and Longhorn in general, is Microsoft's stake in the ground, saying that we believe power on your desktop, locally sitting there doing cool stuff, is here to stay. We're investing on the desktop, we think it's a good place to be, and we hope we're going to start a wave of excitement..."
不是说微软并没有注意到这件事情的发生，他们当然注意到了。当事情弄清楚的时候。他们猛地急刹车了，他们承诺的新技术：例如HTA和DHTML都停在了停在了原地，因特网浏览器团队几乎消失了，他们在若干年之内一直不见踪影。微软根本不会让DHTML之类的技术变得更好，因为这样做对于他们的核心业务来讲太危险了，他们的核心业务就是富客户端。如今微软最大的声音就是微软把整个公司都在赌在了富客户端上面。你可以在讨论Longhorn的每一张幻灯片上发现这一点。Avalon团队的 JoeBeda说道：Avalon和LONGHORN总体说来是微软现在的根本，它告诉世界我们相信桌面的力量，桌面意味着在本地可以做很酷的事情。因此可以说。我们会在桌面系统进行投资，因为我们觉得这是一个好地方，我们希望我们能够开创新一轮的令人激动的…“。

>The trouble is: it's too late.
问题是：已经太晚了。

>I'm a Little Bit Sad About This, Myself
我自己对此也有一点悲伤。


>I'm actually a little bit sad about this, myself. To me the Web is great but Web-based applications with their sucky, high-latency, inconsistent user interfaces are a huge step backwards in daily usability. I love my rich client applications and would go nuts if I had to use web versions of the applications I use daily: Visual Studio, CityDesk, Outlook, Corel PhotoPaint, QuickBooks. But that's what developers are going to give us. Nobody (by which, again, I mean "fewer than 10,000,000 people") wants to develop for the Windows API any more. Venture Capitalists won't invest in Windows applications because they're so afraid of competition from Microsoft. And most users don't seem to care about crappy Web UIs as much as I do.

我自己对此也有一点小伤感，对我而言，网页很好，但是基于网页的应用程序有着很糟糕的延迟；不一致的用户界面；在日常的可用性方面简直就是巨大的退步。如果哪天我日常使用的那些富客户端应用程序Visual Studio, CityDesk, Outlook, Corel PhotoPaint, QuickBooks.都必须使用网页版本的话我简直就会发疯的。但是那就是未来开发人员将会带给我们的。没有人（再次强调，我是指“少于一千万人”）会愿意再给windows系统api进行开发。风险投资不会再愿意投资windows应用程序，因为他们害怕来自微软竞争。并且大部分用户似乎都没有我那样在乎那些不破烂烂的网页界面。

>And here's the clincher: I noticed (and confirmed this with a recruiter friend) that Windows API programmers here in New York City who know C++ and COM programming earn about $130,000 a year, while typical Web programmers using managed code languages (Java, PHP, Perl, even ASP.NET) earn about $80,000 a year. That's a huge difference, and when I talked to some friends from Microsoft Consulting Services about this they admitted that Microsoft had lost a whole generation of developers. The reason it takes $130,000 to hire someone with COM experience is because nobody bothered learning COM programming in the last eight years or so, so you have to find somebody really senior, usually they're already in management, and convince them to take a job as a grunt programmer, dealing with (God help me) marshalling and monikers and apartment threading and aggregates and tearoffs and a million other things that, basically, only Don Box ever understood, and even Don Box can't bear to look at them any more.
王道就是：我注意到了（我也跟一个负责招聘的朋友确认过了）纽约市的懂C++和com编程windows api程序员一年能赚13万美元，而一个典型的使用托管代码语言(Java, PHP, Perl, even ASP.NET)的网页应用程序猿每年赚大概八万美元。这是很大的差别，当我和微软咨询服务的一些朋友讨论这件事情的时候，他们承认说微软已经失去了整整一代的开发者。要花13万美元才能雇佣到那些有COM经验的人的原因就是：在最近的八年内，没有人愿意学习COM编程。所以你必须找一些非常资深的人，这些人通常已经在管理层了。要说服他们从事一个初级程序员的职位。（上帝救救我吧！）让他们处理：序列配置， 监视器， 线程单元模型 以及其他加起来有一百万项零零散散的其他东西， 估计这些东西只有DonBox才懂，而且那怕DonBox也不愿意再去看这些玩意儿了。
 
>Much as I hate to say it, a huge chunk of developers have long since moved to the web and refuse to move back. Most .NET developers are ASP.NET developers, developing for Microsoft's web server. ASP.NET is brilliant; I've been working with web development for ten years and it's really just a generation ahead of everything out there. But it's a server technology, so clients can use any kind of desktop they want. And it runs pretty well under Linux using Mono.
我很不愿意承认有一大堆开发者已经转移到了网页应用开发行列并且不愿意再转回来了。大部分的.NET程序员都是ASP.NET程序员 他们为微软的网页服务器进行开发。ASP.NET 太棒了， 我从事网页应用程序开发已经有十年了。这项技术比所有那些已经有的东西早了整整一代。但是它只不过是一个服务器技术，而且是在LINUX下面用MONO也能运行的很好，在客户端开发者们可以使用任何他们想要的桌面技术。。

>None of this bodes well for Microsoft and the profits it enjoyed thanks to its API power. The new API is HTML, and the new winners in the application development marketplace will be the people who can make HTML sing.

多亏了微软API的力量，所有这些现象都不是微软能够继续享受持续盈利的好兆头。 新的API就是HTML，未来应用程序开发市场的新的赢家肯定是那些能让HTML都唱出动人歌声的人们