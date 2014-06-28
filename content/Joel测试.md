Joel on Software

>#The Joel Test: 12 Steps to Better Code

#Joel测试：12步写出更高质量代码

>######by Joel Spolsky Wednesday, August 09, 2000

---

>Have you ever heard of SEMA ? It's a fairly esoteric system for measuring how good a software team is. No, wait! Don't follow that link! It will take you about six years just to understand that stuff. So I've come up with my own, highly irresponsible, sloppy test to rate the quality of a software team. The great part about it is that it takes about 3 minutes. With all the time you save, you can go to medical school.

你听说过SEMA么？是一种非常深奥的测试软件开发团队水平的系统标准。 等等，先别点开那个链接！那可要花费你约6年的时间去理解。所以我发明了我的“高度不负责”“草率”测试来衡量软件开发团队的质量。 不过这种测试方法的好处是它只需花3分钟。省下来的那些时间，够你再去读个医学院文凭了。



The Joel Test                                               |Joel测试
------------------------------------------------------------|----------
1.	Do you use source control?                              |你们使用代码管理么？
2.	Can you make a build in one step?                       |你们能用一步生成项目版本构建么？
3.	Do you make daily builds?                               |你们每天都做项目版本构建么？
4.	Do you have a bug database?                             |你们有软件错误数据库么？
5.	Do you fix bugs before writing new code?                |你们在写新代码之前会修正之前的代码错误么？
6.	Do you have an up-to-date schedule?                     |你们有最新的日程安排么？
7.	Do you have a spec?                                     |你们有规范么？
8.	Do programmers have quiet working conditions?           |你们的程序员有安静的工作环境么？
9.	Do you use the best tools money can buy?                |你们会使用能花钱买到的最好工具么？
10.	Do you have testers?                                    |你们有测试人员么？
11.	Do new candidates write code during their interview?    |你们在面试的时候会让候选人写代码么？
12.	Do you do hallway usability testing?                    |你们有过道可用性测试么

>The neat thing about The Joel Test is that it's easy to get a quick yesor no to each question. You don't have to figure out lines-of-code-per-day or average-bugs-per-inflection-point. Give your team 1 point for each "yes" answer. The bummer about The Joel Test is that you really shouldn't use it to make sure that your nuclear power plant software is safe.

Joel测试的优点是每个问题很容易都能得到一个“是”或“否”的回答。你不需要去计算 每天代码行数 或者 每转折点软件错误数。每一个“是”的回答就给你的团队加一分。 Joel测试不足的是：你可不要拿它去测试你的核电反应堆控制软件是安全的。

>A score of 12 is perfect, 11 is tolerable, but 10 or lower and you've got serious problems. The truth is that most software organizations are running with a score of 2 or 3, and they need serious help, because companies like Microsoft run at 12 full-time. 

12分满分，11分可以接受，不过低于或等于10分意味着你们团队有严重的问题。 不过事实情况是大部分的软件组织以两到三分运营着。他们急需帮助， 因为像微软这样的公司始终是以12分运营的。

>Of course, these are not the only factors that determine success or failure: in particular, if you have a great software team working on a product that nobody wants, well, people aren't going to want it. And it's possible to imagine a team of "gunslingers" that doesn't do any of this stuff that still manages to produce incredible software that changes the world. But, all else being equal, if you get these 12 things right, you'll have a disciplined team that can consistently deliver.

当然，这些不是衡量软件开发成功或失败的唯一因素：特别是，如果你有个很优秀的团队在开发一个没人想要的产品，恩，人们不会想要的那东西的。而且很难想象一个团队的“高手”不做任何这些条目却仍然能够设法交付能够改变世界的优秀软件。不过，不考虑其他因素，如果你把这12样事情做好了，那么你就拥有一个能够持续交付的纪律严明开发小组。

>###1. Do you use source control? 

###你们使用代码管理么？

>I've used commercial source control packages, and I've used CVS, which is free, and let me tell you, CVS is fine. But if you don't have source control, you're going to stress out trying to get programmers to work together. Programmers have no way to know what other people did. Mistakes can't be rolled back easily. The other neat thing about source control systems is that the source code itself is checked out on every programmer's hard drive -- I've never heard of a project using source control that lost a lot of code.

我使用了商业代码管理包，我使用的是CVS，免费的，而且告诉你，CVS挺好的。 但如果你不用代码管理，你要让程序员协同工作就压力山大了。 程序员无法知道其他人做了什么。 发生错误无法很容易的回滚。 代码管理的另一优点是：源代码本身是被提取到每个程序员自己的硬盘的 – 我从没听说过使用代码管理的项目丢失过一大堆的源代码。

>###2. Can you make a build in one step? 

###你们能一步生成项目构建版本么？

>By this I mean: how many steps does it take to make a shipping build from the latest source snapshot? On good teams, there's a single script you can run that does a full checkout from scratch, rebuilds every line of code, makes the EXEs, in all their various versions, languages, and #ifdef combinations, creates the installation package, and creates the final media -- CDROM layout, download website, whatever.

我这么说的意思是：你们从最新大代码映像构建出一个能发布的编译版本要花多少步？ 在好的团队里，会有一个你能运行的脚本，从头开始完整的检出代码，重新编译每一行代码，生成EXE文件，不管版本，语言，#ifdef预编译宏的组合是怎样。 它能生成安装包，乃至最终的媒体版本—CDROM格式，网站下载之类的。

>If the process takes any more than one step, it is prone to errors. And when you get closer to shipping, you want to have a very fast cycle of fixing the "last" bug, making the final EXEs, etc. If it takes 20 steps to compile the code, run the installation builder, etc., you're going to go crazy and you're going to make silly mistakes.

如果这个过程花费超过一步，那么就容易产生错误。你越是接近发布日期，你就越想以更迅速的的周期去修正“最后”的软件错误，生成最终的可执行文件，等等。 如果要花20步才能编译代码，运行安装构建器，等等。 你就会发疯而且会犯很傻的错误。

>For this very reason, the last company I worked at switched from WISE to InstallShield: we required that the installation process be able to run, from a script, automatically, overnight, using the NT scheduler, and WISE couldn't run from the scheduler overnight, so we threw it out. (The kind folks at WISE assure me that their latest version does support nightly builds.)

因为这个原因，我工作的上家公司从WISE转到了InstallShield:因为我们要求整个安装过程要能使用NT任务调度在晚上自动的从脚本运行，而WISE不能在晚上以计划任务运行，我们就把它给抛弃了。（WISE公司的家伙们向我保证了他们最新的版本确实支持隔夜自动构建）

>###3. Do you make daily builds? 

###你们每天都做项目版本构建么？

>When you're using source control, sometimes one programmer accidentally checks in something that breaks the build. For example, they've added a new source file, and everything compiles fine on their machine, but they forgot to add the source file to the code repository. So they lock their machine and go home, oblivious and happy. But nobody else can work, so they have to go home too, unhappy.

当你在使用源代码管理的时候，有时候一个程序员意外的提交了会导致项目编译构建失败的代码。例如，他们新加了一个源文件，所有东西在他们自己的机器上是能够正确构建的，但是他们忘了把这个源文件提交到代码库了。他们没注意就锁定自己的机器高高兴兴回家去了。但其他人都不能工作了，所以他们也得回家了，不过是不高兴地。

>Breaking the build is so bad (and so common) that it helps to make daily builds, to insure that no breakage goes unnoticed. On large teams, one good way to insure that breakages are fixed right away is to do the daily build every afternoon at, say, lunchtime. Everyone does as many checkins as possible before lunch. When they come back, the build is done. If it worked, great! Everybody checks out the latest version of the source and goes on working. If the build failed, you fix it, but everybody can keep on working with the pre-build, unbroken version of the source.

打破系统正确编译构建的影响是如此之坏（并且很常见），这使得必须创建每天的版本构建来保证没有一次这样的中断会被忽略掉。在大的团队里，一个有效的保证这种中断马上被修正的方法是在每天中午的时候进行日常的版本构建，每个人在饭前都尽可能多的提交自己的工作。当他们吃饭回来，版本构建已经完成，如果构建成功，那太好了！每个人都把代码更新到最新的版本并继续工作。如果版本构建失败了，你就得修正它，但每个人都一个用前一个成功的未被打破的构建继续工作。

>On the Excel team we had a rule that whoever broke the build, as their "punishment", was responsible for babysitting the builds until someone else broke it. This was a good incentive not to break the build, and a good way to rotate everyone through the build process so that everyone learned how it worked. 

在Excel项目里，我们有这样的一个规定，不管谁打破版本构建，作为对他们的“惩罚”，他们必须“照看”版本构建直到其他人打破了版本构建。 这是个很好的初衷让大家不要去打破构建，而且是很好的方法轮换团队里的每个人都通过维护日常构建去学习了解版本构建是如何工作的。

>Read more about daily builds in my article Daily Builds are Your Friend.

你可以通过阅读我的文章 <<日常版本构建是你的好朋友>> 来了解更多。

>###4. Do you have a bug database?

###你们有软件错误数据库么？

>I don't care what you say. If you are developing code, even on a team of one, without an organized database listing all known bugs in the code, you are going to ship low quality code. Lots of programmers think they can hold the bug list in their heads. Nonsense. I can't remember more than two or three bugs at a time, and the next morning, or in the rush of shipping, they are forgotten. You absolutely have to keep track of bugs formally.

不管你说什么。如果你在做代码开发，哪怕是只有一个人的团队，如果你没有一个组织的很好的数据库来罗列代码中的所有错误，你只能交付低质量的代码。 很多程序员觉得他们能够在大脑里罗列所有的软件问题。胡扯。我一次都没办法记得两个或三个错误，而且第二天早晨，或者急着发布，这些问题就被忘掉了。 你必须正式的来追踪管理这些软件错误。

>Bug databases can be complicated or simple. A minimal useful bug database must include the following data for every bug:

>:	complete steps to reproduce the bug

>:	expected behavior

>:	observed (buggy) behavior

>:	who it's assigned to

>:	whether it has been fixed or not

软件错误数据库可以复杂也可以简单。 最精简的可用的软件错误数据库必须为软件错误包含以下数据：

:    重现错误的完整步骤

:    期望的行为

:    实际（错误）行为

:    分配给谁修正

:    是否已经被修正

>If the complexity of bug tracking software is the only thing stopping you from tracking your bugs, just make a simple 5 column table with these crucial fields and start using it.

如果软件错误管理软件的复杂性是唯一让你对追踪软件错误望而却步的因素的话，那就简单的画个5列的包含这些重要数据的表格，就用这个表格就好了。

>For more on bug tracking, read `Painless Bug Tracking`.

你可以阅读我的文章 `无痛苦软件错误跟踪` 来了解更多。

>###5. Do you fix bugs before writing new code? 

###你们在写新代码之前会修正之前的代码错误么

>The very first version of Microsoft Word for Windows was considered a "death march" project. It took forever. It kept slipping. The whole team was working ridiculous hours, the project was delayed again, and again, and again, and the stress was incredible. When the dang thing finally shipped, years late, Microsoft sent the whole team off to Cancun for a vacation, then sat down for some serious soul-searching.

Windows上word的第一个版本被视为是一个“进军死亡”的项目。 花了无限长时间，不断跳票。 整个团队工作时间长的出奇， 项目被一拖再拖，压力无比巨大。几年后， 这个悬着的产品最终被发布的时候，微软把真那个团队送到了坎昆去度假，他们在那儿停下来做些很严肃的“灵魂搜寻（灵修）”活动。

>What they realized was that the project managers had been so insistent on keeping to the "schedule" that programmers simply rushed through the coding process, writing extremely bad code, because the bug fixing phase was not a part of the formal schedule. There was no attempt to keep the bug-count down. Quite the opposite. The story goes that one programmer, who had to write the code to calculate the height of a line of text, simply wrote "return 12;" and waited for the bug report to come in about how his function is not always correct. The schedule was merely a checklist of features waiting to be turned into bugs. In the post-mortem, this was referred to as "infinite defects methodology".

他们后来意识到项目经理是在管理项目的时候行为是如此的不一致，以至于程序员匆匆的结束了编码过程， 写出了及其糟糕的代码，因为修正软件错误不是正式项目安排的一部分。 并没有尝试去降低软件错误数量，相反的，据说有个程序员要编写代码来计算行的高度，简单的写了“return 12；”然后等着软件错误报告进来告诉他这个函数不总是正确。 所谓的进度也不过就是一堆等着变成软件错误的功能列表。 在事后的备忘录中，这被称为“无限软件错误开发方法”。

>To correct the problem, Microsoft universally adopted something called a "zero defects methodology". Many of the programmers in the company giggled, since it sounded like management thought they could reduce the bug count by executive fiat. Actually, "zero defects" meant that at any given time, the highest priority is to eliminate bugs beforewriting any new code. Here's why. 

为了纠正这个问题，微软在全球采用了一种叫做“零缺陷开放方法”。公司很多的程序员偷笑，因为听起来管理层认为他们能够通过执行命令来减少软件错误数量。 实际上，“0缺陷”意味着在任何时候，最优先的始终是消减软件错误，在写任何新的代码之前。 这就是为什么。

>In general, the longer you wait before fixing a bug, the costlier (in time and money) it is to fix.

总而言之，你修正一个软件错误等的时间越长，花费的代价（以时间和金钱衡量）就越大。

>For example, when you make a typo or syntax error that the compiler catches, fixing it is basically trivial.

例如，如果你打错了一个字或者写了个错误语法之类的编译器能发现的错误，修正这类错误几乎不花任何力气。

>When you have a bug in your code that you see the first time you try to run it, you will be able to fix it in no time at all, because all the code is still fresh in your mind.

当你的代码里有一个错误，你尝试去运行的时候第一次发现了它，你几乎不需要花什么时间就能修正这个错误，因为你脑海中关于这段代码的印象还是记忆犹新的。

>If you find a bug in some code that you wrote a few days ago, it will take you a while to hunt it down, but when you reread the code you wrote, you'll remember everything and you'll be able to fix the bug in a reasonable amount of time.

如果你发现了一个你几天前写的代码里的错误，你首先要花写时间定位这个错误，但是当你重新阅读这段你写的代码之后，你就会想起所有东西，你也就能够在合理的时间内修复这个错误。

>But if you find a bug in code that you wrote a few months ago, you'll probably have forgotten a lot of things about that code, and it's much harder to fix. By that time you may be fixing somebody else's code, and they may be in Aruba on vacation, in which case, fixing the bug is like science: you have to be slow, methodical, and meticulous, and you can't be sure how long it will take to discover the cure.

但如果你发现了一个你几个月前写的代码， 你很可能已经忘记了那段代码大部分的东西了， 修正起来这就变得困难多了。 那个时候你也可能在修正他人的错误，而他们可能在阿鲁巴岛度假，这种情况下要修正这种错误就像科学一样：你得慢一点，方法性的，小心翼翼的，而且你无法确定到底要花多长时间才能找到修正方案。

>And if you find a bug in code that has already shipped, you're going to incur incredible expense getting it fixed.

如果你在已经发布的代码里找到了一个错误，你就要花费难以估量的代价来修正那个错误。

>That's one reason to fix bugs right away: because it takes less time. There's another reason, which relates to the fact that it's easier topredict how long it will take to write new code than to fix an existing bug. For example, if I asked you to predict how long it would take to write the code to sort a list, you could give me a pretty good estimate. But if I asked you how to predict how long it would take to fix that bug where your code doesn't work if Internet Explorer 5.5 is installed, you can't even guess, because you don't know (by definition) what'scausing the bug. It could take 3 days to track it down, or it could take 2 minutes.

那就是要马上修正错误的一个原因：因为这样花更少时间。 还有个原因，牵涉到这样的一个事实：也就是预测要花多长时间写新代码总比预测要花多长时间修正代码要简单。例如，如果我问你要花多长时间来写个排序链表的代码，你能给一个相当不错的估算。但我要是问你要花多少时间修正个软件错误，该错误导致你的代码在IE5.5版本安装后无法工作，你甚至连猜都无法猜，因为你不知道（从定义上）什么在导致这个问题。可能要花3天才能定位这个错误，也可能只要两分钟。

>What this means is that if you have a schedule with a lot of bugs remaining to be fixed, the schedule is unreliable. But if you've fixed all the known bugs, and all that's left is new code, then your schedule will be stunningly more accurate.

这意味着如果你的计划上有大量等着修复的软件错误，那么计划就是不可靠的。但如果你已经修正了所有已知的软件错误，剩下的全是新代码开发的话，那么你的计划相比而言就会可靠的多。

>Another great thing about keeping the bug count at zero is that you can respond much faster to competition. Some programmers think of this as keeping the product ready to ship at all times. Then if your competitor introduces a killer new feature that is stealing your customers, you can implement just that feature and ship on the spot, without having to fix a large number of accumulated bugs.

保持软件错误数为零的另一大优势在于，你能够更迅速的响应竞争。有些程序员将其视为保证产品随时处于发布状态。这样一旦你的对手引入了“杀手”级新特性偷走你的客户，你就可以马上实现那个特性然后马上发布，而不需要修正一大堆积累的软件错误。

>###6. Do you have an up-to-date schedule? 

###你们有最新的日程安排么？

>Which brings us to schedules. If your code is at all important to the business, there are lots of reasons why it's important to the business to know when the code is going to be done. Programmers are notoriously crabby about making schedules. "It will be done when it's done!" they scream at the business people.

这就提到了日程安排，如果你们的代码对于业务很重要，为什么让业务部门知道代码时候能够完成很重要就有很多答案了，程序员做日程安排是出了名的差。“做好的时候就好了啊”他们总会对业务部门的人这样吼道。

>Unfortunately, that just doesn't cut it. There are too many planning decisions that the business needs to make well in advance of shipping the code: demos, trade shows, advertising, etc. And the only way to do this is to have a schedule, and to keep it up to date.

不幸的是，不仅仅这个原因，还有很多计划上的决定使得业务部门必须提前知道代码交付的日期，例如：产品展示，交易展示，广告等。唯一完成这些的方法就是要做日程安排，并且实时更新这些安排。

>The other crucial thing about having a schedule is that it forces you to decide what features you are going to do, and then it forces you to pick the least important features and cut them rather than slipping intofeaturitis (a.k.a. scope creep).

制定日程安排的另一个至关重要点是，他迫使你们决定要实现哪些特性，然后它就迫使你们挑出那些最无关紧要的特性扔掉，而不是把它塞进项目框架里

>Keeping schedules does not have to be hard. Read my article Painless Software Schedules, which describes a simple way to make great schedules.

保持进度不一定就是很困难的，可以读读我的文章 “无痛软件进度安排“， 描述了制定完美计划的最简单方法。

>###7. Do you have a spec? 

###你们有规范么？

>Writing specs is like flossing: everybody agrees that it's a good thing, but nobody does it. 

写规范就像用牙线洁牙:每个人都同意这是件好事情，不过就是没人去做。

>I'm not sure why this is, but it's probably because most programmers hate writing documents. As a result, when teams consisting solely of programmers attack a problem, they prefer to express their solution in code, rather than in documents. They would much rather dive in and write code than produce a spec first.

我不知道为什么，但是大概所有的程序员都痛恨写文档。因此，当一个团队里全部是攻坚问题的程序员的时候，他们更倾向于使用代码来表达他们的解决方案，而不是写文档。他们更倾向于马上上手写代码而不是先写出个规范文档。

>At the design stage, when you discover problems, you can fix them easily by editing a few lines of text. Once the code is written, the cost of fixing problems is dramatically higher, both emotionally (people hate to throw away code) and in terms of time, so there's resistance to actually fixing the problems. Software that wasn't built from a spec usually winds up badly designed and the schedule gets out of control.  This seems to have been the problem at Netscape, where the first four versions grew into such a mess that management stupidly decided to throw out the code and start over. And then they made this mistake all over again with Mozilla, creating a monster that spun out of control and took several years to get to alpha stage.

>My pet theory is that this problem can be fixed by teaching programmers to be less reluctant writers by sending them off to takean intensive course in writing. Another solution is to hire smart program managers who produce the written spec. In either case, you should enforce the simple rule "no code without spec".

在设计阶段，如果你发现问题，你可以很容易的编辑几行文字就解决这个问题。 一旦代码写完了，要解决问题的大家就高了无数倍，无论是从情感角度出发（人们讨厌舍弃写完的代码）还是从时间角度，因此实际上修正问题的时候还有一种抵制性。非软件规范构建出的软件通常会设计的不好而且进度失去控制。这似乎是网景公司曾经遇到过的问题，前4个发布已经进展得一团糟的时候，管理层愚蠢的决定扔掉所有的代码重头开始。然后Mozilla重新完整的犯了这个错误，创建了一个失去控制的怪物，花了数年将其推进到Alpha发布阶段。我的简单观点是这个问题可以通过将程序员送去参加高强度的写作训练使他们不那么不愿意写作而得以解决。另一个解决方案是雇佣聪明的项目经理来编写规范。不管哪一种方法，你必须确保这个简单的规定“没有规范，不写代码”

>Learn all about writing specs by reading my 4-part series.

阅读我的 “4部分系列” 来学习关于写规范的所有详情

>###8. Do programmers have quiet working conditions? 

###你们的程序员有安静的工作环境么？

>There are extensively documented productivity gains provided by giving knowledge workers space, quiet, and privacy. The classic software management book Peopleware documents these productivity benefits extensively.

大量研究表明，给予员工空间，安静的环境和隐私空间能够极大的提高工作效率。 经典的软件管理书籍“人件”提到这些生产力效益改善是很可观的。

>Here's the trouble. We all know that knowledge workers work best by getting into "flow", also known as being "in the zone", where they are fully concentrated on their work and fully tuned out of their environment. They lose track of time and produce great stuff through absolute concentration. This is when they get all of their productive work done. Writers, programmers, scientists, and even basketball players will tell you about being in the zone.

问题是，大家都知道脑力劳动者最佳工作状态是进入“工作流”（也即进入“状态”），那种状态下能够完全集中在他们的工作上并且“脱离”出所处的工作环境。 他们不再在意时间并且能够通过高度的注意力集中产生极佳的工作成果。这就是他们能够把他们的创造性工作完成的时候。作家，程序员，科学家甚至是篮球运动员都会告诉你他们所处的那种“状态”。

>The trouble is, getting into "the zone" is not easy. When you try to measure it, it looks like it takes an average of 15 minutes to start working at maximum productivity. Sometimes, if you're tired or have already done a lot of creative work that day, you just can't get into the zone and you spend the rest of your work day fiddling around, reading the web, playing Tetris.

问题是，要进入这种“状态”可不容易。 如果你尝试衡量它，看起来像是要达到最佳工作状态平均要花15分钟。 有时，如果你已经很累活着你已经进行了大量的创作性劳动，你就无法再进入那种状态，剩下的工作日你就会：到处闲逛，上网，玩俄罗斯方块等等。

>The other trouble is that it's so easy to get knocked out of the zone. Noise, phone calls, going out for lunch, having to drive 5 minutes to Starbucks for coffee, and interruptions by coworkers -- especiallyinterruptions by coworkers -- all knock you out of the zone. If a coworker asks you a question, causing a 1 minute interruption, but this knocks you out of the zone badly enough that it takes you half an hour to get productive again, your overall productivity is in serious trouble. If you're in a noisy bullpen environment like the type that caffeinated dotcoms love to create, with marketing guys screaming on the phone next to programmers, your productivity will plunge as knowledge workers get interrupted time after time and never get into the zone.

另一个问题是，要脱离这种状态是如此容易。 噪音，电话，出去吃饭，要开5分钟车去星巴克喝咖啡，来自其他同事的打扰 – 特别是来自同事的打扰 – 所有这些都能把你拖出状态区。 如果你同事问了你一个问题，1分钟的间断， 但是这是如此严重的扰乱了你的状态，以至于你要重新回到状态要花半个小时， 这样你的整体工作效率就非常堪忧了。如果你在工作在那种咖啡因.COM 创业人员喜欢创建的那种格子式的工作空间里，程序员旁边的销售人员在电话里大声吼叫，你的工作效率就会急剧下降因为你时不时的就会被打断，永远无法进入状态。

>With programmers, it's especially hard. Productivity depends on being able to juggle a lot of little details in short term memory all at once. Any kind of interruption can cause these details to come crashing down. When you resume work, you can't remember any of the details (like local variable names you were using, or where you were up to in implementing that search algorithm) and you have to keep looking these things up, which slows you down a lot until you get back up to speed.

对程序员来说，这特别困难。效率受制于一次性你在记忆中处理一大堆小细节的能力。 任何中断都可能导致这些小细节的丢失。 当你回到工作中来的时候，你无法想起一些细节（例如你正在使用的局部变量的名字，或者你在实现一个搜索算法的时候已经进行到什么地步了） 然后你就必须不停的去查找这些东西， 这就会急速降低你的处理速度知道你重新回到状态上来。

>Here's the simple algebra. Let's say (as the evidence seems to suggest) that if we interrupt a programmer, even for a minute, we're really blowing away 15 minutes of productivity. For this example, lets put two programmers, Jeff and Mutt, in open cubicles next to each other in a standard Dilbert veal-fattening farm. Mutt can't remember the name of the Unicode version of the strcpy function. He could look it up, which takes 30 seconds, or he could ask Jeff, which takes 15 seconds. Since he's sitting right next to Jeff, he asks Jeff. Jeff gets distracted and loses 15 minutes of productivity (to save Mutt 15 seconds).

这里有个简单的代数运算。让我们假定（有证据表明）如果我们打断了一个程序员，哪怕只有一分钟，我们就毁掉了15分钟的工作效率。在这个例子里，我们假设与两个程序员，Jeff和Mutt，相邻地坐在“标准呆伯特小牛育肥农场”的格子间里。Mutt记不起strcpy函数的Unicode版本函数了，他可以查一下的，大约要花30秒钟，或者他可以问一下Jeff，大约要花15秒钟，因为他就坐在Jeff旁边，所以他就问了Jeff，Jeff分了下心然后就丢失了15分钟能够的工作效率（以换取Mutt的15秒）。

>Now let's move them into separate offices with walls and doors. Now when Mutt can't remember the name of that function, he could look it up, which still takes 30 seconds, or he could ask Jeff, which now takes 45 seconds and involves standing up (not an easy task given the average physical fitness of programmers!). So he looks it up. So now Mutt loses 30 seconds of productivity, but we save 15 minutes for Jeff. Ahhh!

现在让我们把他们换进有墙有门的办公室里。现在当Mutt记不得那个函数名字的时候，他可以查一下，约花30秒钟，或者他可以去问Jeff，现在要45秒了，而且还要站起来（考虑到程序员的平均体重，这可不是什么简单的事儿）。所以他就决定自己查了。所以Mutt现在损失了30秒钟的效率，但是我们挽救了Jeff的15分钟效率。啊！

>###9. Do you use the best tools money can buy? 

###你们会使用能花钱买到的最好工具么？

>Writing code in a compiled language is one of the last things that still can't be done instantly on a garden variety home computer. If your compilation process takes more than a few seconds, getting the latest and greatest computer is going to save you time. If compiling takes even 15 seconds, programmers will get bored while the compiler runs and switch over to reading The Onion, which will suck them in and kill hours of productivity.

写编译型语言代码是做后几项无法在一系列各种家用计算机上无法完成的最后几项事情之一。如果编译过程不止花费几秒钟，那么购买最新最强大的计算机还是能节省你时间的。如果编译过程花了15秒钟，那么编译运行的时候程序员就会不耐烦，跑去读其他东西，这会把他们拖出效率去浪费他们甚至是几个小时的工作效率。

>Debugging GUI code with a single monitor system is painful if not impossible. If you're writing GUI code, two monitors will make things much easier.

使用单显示器系统调试界面代码并不是不可能但是是非常痛苦的事情。如果你在编写界面代码，双显示器会让事情简单很多。

>Most programmers eventually have to manipulate bitmaps for icons or toolbars, and most programmers don't have a good bitmap editor available. Trying to use Microsoft Paint to manipulate bitmaps is a joke, but that's what most programmers have to do.

很多程序员甚至要处理图标的位图或者工具栏，但是大部分的程序员并没有很好的位图编辑器。尝试使用微软的画图软件处理位图听起来就象个笑话，不过这就是大部分程序员要做的。

>At my last job, the system administrator kept sending me automated spam complaining that I was using more than ... get this ... 220 megabytes of hard drive space on the server. I pointed out that given the price of hard drives these days, the cost of this space was significantly less than the cost of the toilet paper I used. Spending even 10 minutes cleaning up my directory would be a fabulous waste of productivity.

我上一份的工作，系统管理员会发送自动的垃圾邮件向我抱怨说我已经使用了超过…听听看…220兆的服务器硬盘存储空间。 我指出，考虑到现在存储的价格，这些空间的价格要比我使用的厕纸的价格都要便宜的多。 花费10分钟来清理我的文件夹就是巨大的效率浪费。

>Top notch development teams don't torture their programmers. Even minor frustrations caused by using underpowered tools add up, making programmers grumpy and unhappy. And a grumpy programmer is an unproductive programmer.

顶尖的开发团队不会折磨他们的程序员，哪怕是使用不够强大的工具带来的小小挫折感都能够使程序员暴躁，不高兴。而一个暴躁的程序员肯定是一个没什么效率的程序员。

>To add to all this... programmers are easily bribed by giving them the coolest, latest stuff. This is a far cheaper way to get them to work for you than actually paying competitive salaries!

最后再说一点：通过给程序员使用最新最酷的东西很容易就能贿赂程序员，比起有竞争力的薪水这是个便宜的多的方法来说服让程序员为你工作。

>###10. Do you have testers? 

###你们有测试人员么？

>If your team doesn't have dedicated testers, at least one for every two or three programmers, you are either shipping buggy products, or you're wasting money by having $100/hour programmers do work that can be done by $30/hour testers. Skimping on testers is such an outrageous false economy that I'm simply blown away that more people don't recognize it.

如果你的团队没有专门的测试人员，至少每两到三人配备一个测试人员，要么你们将交付有错误的产品，要么你们就要花费$100/小时让程序员给你做测试，而不是花费$30/小时让测试人员来做测试。 克扣测试人员配备是我难以理解的伪经济学，而更多的人则是没有意识到这个问题。

>Read Top Five (Wrong) Reasons You Don't Have Testers, an article I wrote about this subject.

你可以阅读我写的关于这个主题的另一篇文章“5个你不需要测试人员的最大（错误）理由”

>###11. Do new candidates write code during their interview? 

###你们在面试的时候会让候选人写代码么？

>Would you hire a magician without asking them to show you some magic tricks? Of course not.

你会不让魔术师表演点儿魔术就雇佣他为魔术师么？当然不会。

>Would you hire a caterer for your wedding without tasting their food? I doubt it. (Unless it's Aunt Marge, and she would hate you forever if you didn't let her make her "famous" chopped liver cake).

你会不尝试下食物就帮你的婚礼找个餐饮服务么？我有点怀疑。（除非是Marge阿姨，如果你不让她做她“著名”的切肝蛋糕，她会一辈子都怀恨在心的）。

>Yet, every day, programmers are hired on the basis of an impressive resumé or because the interviewer enjoyed chatting with them. Or they are asked trivia questions ("what's the difference between CreateDialog() and DialogBox()?") which could be answered by looking at the documentation. You don't care if they have memorized thousands of trivia about programming, you care if they are able to produce code. Or, even worse, they are asked "AHA!" questions: the kind of questions that seem easy when you know the answer, but if you don't know the answer, they are impossible.

然而，每天都有程序员被雇佣，因为有出色的简历以及面试官很享受跟他们聊天。 或者要么就是问些简单的问题（“CreateDialog()和DiagBox()有什么区别啊？”） 这个问题通过看文档就能够回答的。 你并不在意他们是否熟记成千山万的编程技巧，你只关心他们是否能写出代码。或者，更糟，他们会被问“啊！”系列问题：这种问题如果你知道答案那就很简单，如果你不知道，那基本就不可能。

>Please, just stop doing this. Do whatever you want during interviews, but make the candidate write some code. (For more advice, read myGuerrilla Guide to Interviewing.)

请不要这样做。 面试的时候可以做任何你想做的，但是请务必让面试对象写几行代码。（更多的建议，请阅读我的突击面试指南）

>###12. Do you do hallway usability testing? 

###你们有过道可用性测试么？

>A hallway usability test is where you grab the next person that passes by in the hallway and force them to try to use the code you just wrote. If you do this to five people, you will learn 95% of what there is to learn about usability problems in your code.

过道可用性测试是指，你随机的逮住下一个经过过道的人然后迫使他们去使用你刚写的代码。如果你对5个人做了这个测试，你就会学到你代码里95%潜在的可用性问题。

>Good user interface design is not as hard as you would think, and it's crucial if you want customers to love and buy your product. You can read my free online book on UI design, a short primer for programmers.

好的用户交互设计并没有你想的那么难，但是他对于让你的客户爱上你的产品乃至购买却是至关重要的。 你可以阅读的我的关于界面设计的免费在线书籍“程序员界面设计简介”

>But the most important thing about user interfaces is that if you show your program to a handful of people, (in fact, five or six is enough) you will quickly discover the biggest problems people are having. ReadJakob Nielsen's article explaining why. Even if your UI design skills are lacking, as long as you force yourself to do hallway usability tests, which cost nothing, your UI will be much, much better.

对于用户界面最重要的事情是，如果你向一小堆人（实际5-6人就够了）展示你的程序，你就会很快的发现人们会遇到的最大问题。 阅读Jakob Nielsen的文章了解为什么。 即使你的缺乏UI设计技能，只要你迫使自己去做过道可用性测试，基本不花什么代价，你的UI就会变得好很多很多。

