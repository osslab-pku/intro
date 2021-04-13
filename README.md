# 研究方向介绍

## 引言

## 先置知识

如果你之前没有研究经历，我强烈推荐在开始做一个研究课题前，将以下列表中的文章通读一遍。这些文章均为计算机各个领域的知名学者撰写的教程性质的文章，内容涵盖：做研究的基本方法论；研究生阶段应该做和不应该做的事情；如何写论文；如何最大化文章被接受的概率；如何做报告；等等。文章列表摘自[刘譞哲](liuxuanzhe.com)老师的官网。由于我认为以上内容对研究生应当是**常识性**的，本文不会对以上内容做出更多的介绍。此外，在有一些研究经历之后，也可以选择你疑惑的内容再读一遍，通常会有更多的收获。

* [The Three Golden Rules for Successful Scientific Research](http://www.cs.utexas.edu/~EWD/ewd06xx/EWD637.PDF) (by Prof. E.W. Dijkstra)
* [Some Modest Advice for Graduate Students](https://stearnslab.yale.edu/modest-advice) (by Prof. Stephen C. Stearns)
* [How to Write a Good Research Paper](http://spoke.compose.cs.cmu.edu/write/) (by Prof. Mary Shaw)
* [Common Advice on Writing Research Papers](http://taoxie.cs.illinois.edu/publications/writepapers.pdf) (by Prof. Tao Xie)
* [How/How Not to Write a Good System Paper](https://www.usenix.org/legacy/publications/library/proceedings/dsl97/good_paper.html) (by Dr. Roy Levin and Dr. David D. Redell)
* [Preliminary Guidelines for Empirical Research in Software Engineering](http://dl.acm.org/citation.cfm?id=636197) (by Prof. Barbara Kitchenham et al.)
* [Why I gave your paper a Strong Accept](http://matt-welsh.blogspot.hk/2016/04/why-i-gave-your-paper-strong-accept.html) (by Matt Welsh)
* [Why I gave your paper a Strong Reject](http://matt-welsh.blogspot.hk/2016/04/why-i-gave-your-paper-strong-reject.html) (by Matt Welsh)
* [You and Your Research](http://www.cs.virginia.edu/~robins/YouAndYourResearch.html) (by Prof. Richard Hamming) （这篇的主题是：如何做出**卓越**的研究）
* [How to Give a Technical Presentation](http://homes.cs.washington.edu/~mernst/advice/giving-talk.html) (by Prof. Michael Ernst)

然后，在进入具体的研究方向介绍之前，我试图先给出一个大的绘图(big picture)。一般而言，这个世界上的所有研究可以分为两类：**发明型研究**(Solution-Seeking Research)和**发现型研究**(Knowledge-Seeking Research)。就软件工程领域而言，可以将两类研究的区别总结于下表：

|            | 发现型研究                                                   | 发明型研究                                                   |
| ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **目标**   | 提出一些观点(claim)，并使用科学的方法证明你的观点。这些观点一经证实，可以用于指导软件开发**实践**，从而提升软件开发的**效率**或**质量** | 设计一个解决方案， 或改进现有的解决方案，以解决一个特定的**实际**问题，从而提升软件开发的**效率**或**质量** |
| **聚焦点** | 软件开发过程中的某种（尚不清楚或不广为人知的）现象           | 特定场景下的实际问题，以及解决这些问题的阻碍                 |
| **产出**   | 一组**首次**经过科学方法证实的结论。在分析过程中，可能也会产出一些解决方案，例如一种数据分析流程，或者用于某种估算的算法等 | 一个**新**的解决方案（算法、系统、模型、工具等），以及对这个解决方案的系统性验证 |
| **举例**   | 什么样的人可以成为开源社区中的长期贡献者[1]？代码审查的难点和好处究竟在哪里[2]？什么样的开源项目会失败[3]？ | 如何对包含多过程调用的程序的性质进行精确的分析[4]？如何对复杂程序生成更容易找到bug的测试样例[5]？如何自动检测代码与注释的不一致[6]？ |

* **表格改编自**：Stol, Klaas-Jan, and Brian Fitzgerald. "The ABC of software engineering research." ACM Transactions on Software Engineering and Methodology (TOSEM) 27.3 (2018): 1-51. （这篇文章对软件工程研究中，**发现型研究**的研究范式做出了全面和深入的介绍，思路广阔，不局限于目前主流的数据分析类研究，有一些研究经历之后可以通读一遍参考参考）
* 举例的文献列表：
  1. Zhou, Minghui, and Audris Mockus. "What make long term contributors: Willingness and opportunity in OSS community." *2012 34th International Conference on Software Engineering (ICSE)*. IEEE, 2012.
  2. Bacchelli, Alberto, and Christian Bird. "Expectations, outcomes, and challenges of modern code review." *2013 35th International Conference on Software Engineering (ICSE)*. IEEE, 2013.
  3. Valiev, Marat, Bogdan Vasilescu, and James Herbsleb. "Ecosystem-level determinants of sustained activity in open-source projects: A case study of the PyPI ecosystem." *Proceedings of the 2018 26th ACM Joint Meeting on European Software Engineering Conference and Symposium on the Foundations of Software Engineering*. 2018.
  4. Reps, Thomas, Susan Horwitz, and Mooly Sagiv. "Precise interprocedural dataflow analysis via graph reachability." *Proceedings of the 22nd ACM SIGPLAN-SIGACT Symposium on Principles of Programming Languages*. 1995.
  5. Cadar, Cristian, Daniel Dunbar, and Dawson R. Engler. "Klee: unassisted and automatic generation of high-coverage tests for complex systems programs." *OSDI*. Vol. 8. 2008.
  6. Tan, Lin, et al. "/* iComment: Bugs or bad comments?*/." *Proceedings of the 21th ACM SIGOPS Symposium on Operating Systems Principles*. 2007.

上表中有一些加粗的内容需要特别注意。首先，一个研究应当是在某种方面，做到了一些**全新的**(novel)，前人没有做过的事情。比如说，如果一个人声称因为牛顿和莱布尼兹发明了微积分，因此X国对此没有自主知识产权，所以他”发明“了一种本质上和微积分完全一样的”细巨分“，这种重复发明就不属于科学研究的范畴；而如果有人发现牛顿和莱布尼兹的微积分对无穷小没有一个严谨的定义，并发展了新的理论来给出严谨定义，这就属于科学研究的范畴。

其次，一个研究要得到承认，就必须**符合某个研究社区(community)的价值取向**。对于所有的工程学科而言，研究必须是为了**解决实际问题**而出发的。你试图解决的问题必须**不能是一个空想的、实际不存在的伪问题**。郭德纲的著名段子可以作为伪问题的经典例子：

> 内行要是和外行去辩论那就外行!
>
> 比如我和火箭科学家说，你那火箭不行，燃料不好，我认为得烧柴，最好是煤，煤还得选精煤，水洗煤不好。
>
> 如果那科学家，要是拿正眼看我一眼，那他就输了!

“发射火箭应该烧柴、水洗煤、还是精煤？”就是一个典型的伪问题。为了不至于提出一个伪问题，**工程学科的研究者必须首先是一个合格的工程师**，具备一个同领域工程师应当具备的大多数知识和技能。当然，实际研究中，判断一个问题是不是伪问题不仅可能非常困难，也可能会有很多争议的。有的问题并不是完全没有价值，而是价值非常局限；有的问题可能一开始不被人认为有价值，之后却产生了非常深远的影响。为了你的文章能够发表，如果你的问题看上去不像是具有实际价值的问题，那么你可能需要花更多的篇幅去**论证**为什么你解决的问题具有实际价值，或者为什么解决这个问题具有带来实际价值的潜力。论证的方法可以是引用前人的研究；详细描述一个读者可能不知道的真实世界的应用场景；甚至可以让研究的一部分篇幅专门用于回答“为什么此问题具有价值？”这个问题。

对软件工程而言，软件工程领域关心的问题是如何提升软件开发的**效率**与**质量**。如果你发现你的研究问题不符合此标准，但是看上去也是有价值的，那么可能你需要寻找看重你的研究价值的方向，并投稿到相应的会议或期刊。此外，作为同行评审制度的副作用，每一个领域都会产生自己的**品味(taste)**，尽管审稿人的偏好可能会使得一些有意义的研究无法得到发表。把控一个研究社区品味的最好方式，就是与这个领域中有一定积累的学者进行合作。

## 研究领域

我们实验室长期而来一直聚焦于在软件工程领域进行**发现型**的研究。为什么软件工程领域需要发现型的研究，而不仅仅是去开发算法、系统与工具呢？第一个原因是，软件开发虽然以数学作为理论基础，并由计算机技术加以支撑，但是**归根结底还是人的活动**。比如说，开发一个软件不仅需要**人**与**技术**进行**极其复杂而又不能出错的交互**；也需要**人**与**人**之间进行**交流**与**组织**；还需要降低技术的**门槛**（例如控制代码的复杂度、编写技术文档等），使得不那么聪明的人也能参与软件开发。由于我们对人类智能的有限认识，这些问题是难以采用数学的方法去解决的，需要通过对历史事件的分析与反思，反复迭代得到最优的解决方案。第二个原因是，真实的软件开发场景极端复杂，很多问题也不太可能存在一个通用的解决方案(Silver Bullet)，使得**定义合适的技术问题本身就不太容易**，需要科学的证据和观点加以支持。因此，如果没有发现型的研究对**软件工程研究**和**软件开发实践**做出科学的指导，人们可能会在伪技术问题上浪费时间，拍脑袋的管理决策也可能会产生非常可怕的后果。感兴趣的读者可以看一看《人月神话》这本书，了解上世纪60年代IBM开发操作系统时遇到的各种问题。同时期的著名计算机科学家Edsger W. Dijkstra曾经这么评论过当时的“软件工程”：

> The required techniques of effective reasoning are pretty formal, but as long as programming is done by people that don't master them, the software crisis will remain with us and will be considered an incurable disease. And you know what incurable diseases do: they invite the quacks and charlatans in, who in this case take the form of Software Engineering gurus. (翻译：写代码需要很高的姿势水平，可是写代码的人一般都是傻Ｘ，所以他们总是写不出好软件。总是写不出来，就会引来一帮“软件工程”砖家；但是砖家们的观点啊，都too young, too simple, sometimes naïve!)

当然，随着软件行业近六十年的发展，现在我们已经没有所谓的“软件危机”，倒不如说处在一个“傻Ｘ竟然也能开发软件”的时代。借助各种软件开发工具和成熟开源生态系统的支持，从小学生到北大青鸟速成班学员，都能在很短的时间内写出实际可用的应用程序。软件行业能走到今天，终究离不开众多软件行业实践者和软件工程研究人员的共同努力。

为了进行发现型的研究，需要采用某种研究范式。发现型研究有很多常用的研究范式，比如实地调研(Field Study)、实验室实验、计算机模拟等等，关于这些范式的详细介绍可以参考上一个表格的出处文章。然而，出于领域的特点，目前大多数软件工程领域的发现型研究都属于**实地调研**，而且主要是通过**观测已有的软件开发活动数据**，或者通过**访谈/发问卷调查相关的人员**来完成。控制变量实验相对较少见，主要原因在于软件开发的高成本和不可控性，使得这种实验不仅在成本上难以接受，也很难得到贴近现实的结果。由于软件开发活动不仅极端复杂还包含人类参与，基本没有采用计算机模拟来回答实际问题的研究。

上述加粗的两种研究方法之所以能成为主流范式，主要是要感谢近年来**开源软件**的流行与成功。由于开源软件普遍奉行数据开放的原则，且成功的开源软件往往具有极高的代码质量和项目管理水平，从而这些开源软件项目提供了**海量的真实软件开发活动数据**，从而能够用于回答之前由于缺乏数据而难以回答的大量问题（使用企业数据去做公开发表的研究往往是比较困难的）。于此同时，**“开源”这个模式本身，也带来了大量的全新问题**，例如开源项目要如何可持续发展，企业要如何参与开源等等。

具体到我们实验室的研究而言，我们的**研究对象**主要是开源软件的软件开发活动数据；**研究目标**通常是观察和度量大规模软件项目或生态中人们的开发行为，量化开发者与其环境和软件制品之间的关系，以期理解和掌握控制大型复杂软件系统的方法；**研究风格**通常是从某一个软件开发中普遍存在的实际问题出发，利用数据挖掘与分析对问题本身进行深入和全面的探索；如有必要，通过访谈和问卷验证我们的结论；如有可能，基于前面的结果尝试进行量化与建模，使用模型验证我们的结论，并建立推荐工具，对软件开发各种实践活动进行预测和推荐。

我们常常使用**开源软件量化分析**这个词来总结，也可以使用以下关键词来总结我们实验室当前的研究领域：

| 一级学科       | 软件工程（Software Engineering）                      |
| -------------- | ----------------------------------------------------- |
| 细分领域关键词 | 数据驱动的软件开发（Data-Driven Software Development) |
|                | 软件仓库挖掘（Mining Software Repositories）          |
|                | 软件度量（Software Measurement）                      |
|                | 实证/经验软件工程（Empirical Software Engineering）   |
|                | 软件数字社会学（Software Digital Sociology）          |
|                | 软件数字考古学（Software Digital Archeology）         |

## 研究对象

之前提到，我们实验室的主要研究对象是**软件开发活动数据**。这是一个非常宽广的概念。一般而言，只要是在软件开发过程中产生的数据，都可以称作软件开发活动数据，包括但不限于

* **源代码(Source Code)**：对于开源软件而言，代码显然是最容易获取到的数据，也是最重要的基础数据。有研究可以仅仅观察源代码来总结开发者的使用模式，例如：开发者如何在Java中使用继承(Stevenson and Wood, ICSE 2018)？什么样的Python代码才是“Pythonic”的代码(Peng et al., SANER 2021)？等等。当然，更多的时候，源代码是作为基础数据，与其他数据相结合来回答各种复杂的问题，例如与版本控制数据相结合来研究代码重构，等等。
* **Documentation**: Comment, API Documentation, Tutorial, Workflow Documentation, etc
* **Configuration Files**: Dependency Config, CI/CD Config, Quality Assurance Config, etc
* **Changes** and Documentation Accompanying Changes (in Version Control Systems): Commits, Releases, File Diffs, Commit Messages, Release Notes, etc
* **GitHub**: Issues, PRs, Release Notes, Users, Organizations, etc
* **Package Hosting Platforms**: Maven, npm, PyPI, etc
* **Social Websites**: Stack Overflow, Twitter, Slack, etc
* **Issue Tracking System**: JIRA, Bugzilla
* **Email Archives**

## 研究问题

但凡软件工程领域，任何研究问题都需要与提高开发效率和软件质量相关，即相关性（relevant）。另外需要具有的特点：

1. 前沿性(novel)：选题应聚焦于有新意的问题，进行创新和深入的研究。

2. 普遍性(non-trivial)：问题和解决方案需要有一般性，不能只针对极个别群体。

我们的研究主要围绕着**开源软件**与**开源社区**，使用这些数据来解答**代码**、**文档**、**社区**与**生态**有关的问题。关于我们正在研究的具体问题，可以参考“推荐文献”一节中后面的列表。

## 研究方法

### 数据集

大量研究会直接使用GitHub上的项目数据，也有一些非常常用的公开数据集，例如Libraries.io, GHTorrent, World of Code等。此外，互联网上成千上万开源项目的数据都是开放的，可获取的软件开发活动数据非常多。一般来说，开源项目都会支持在线问题追踪系统，版本控制系统和邮件列表等，例如[Mozilla 的在线issue tracking system](https://bugzilla.mozilla.org/show_bug.cgi?id=1000000)、[Linux kernel 的在线代码库(mainline code repository)](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git)、[Linux kernel 的在线邮件列表(mailing-list)](https://lkml.org/)等。可以编写爬虫，面对你的实际研究问题，获取各种各样的数据。

### 分析方法

我个人认为，使用什么样的分析方法，完全取决于你手边正在进行的课题的情况。一般而言，要得到简单的描述性结果，按直觉进行简单的数据分析与可视化即可；如果要得到相关性或者因果的结论，则需要用到各种统计学工具，例如相关性分析、回归分析、显著性检验等等；如果需要对复杂现象进行系统性的描述与总结，一般则采用某种定性研究的方法，例如主题分析(Thematic Analysis)等。

本文不想过多地局限于介绍某些具体的工具，一方面是因为，为了进行某种分析去自学相关工具应当是一个必备技能；另一方面，不同人对不同工具有不同的偏好，使用的效率往往也是不一样的。这里提供一个（并不完整的）常用工具列表：

* 原始数据处理：Shell Scripts, Perl, Python

* 数据分析：R language, Python + pandas + matplotlib + Seaborn, Jupyter Lab

* 定性分析：interviews, surveys, open coding, thematic analysis

## 推荐阅读

### 领域科普文章

1. Brooks Jr, Frederick P. *No Silver Bullet – Essence and Accident in Software Engineering*. April, 1987.
2. Brooks Jr, Frederick P. *The Mythical Man-Month: Essays on Software Engineering*. Pearson Education, 1995.
3. 邹欣. 构建之法: 现代软件工程. 人民邮电出版社. 2017年6月.
4. 周明辉, 郭长国. 基于大数据的软件工程新思维.  中国计算机学会通讯. 第十卷第3期. 2014年3月.
5. 周明辉, 张伟等. 开源软件的量化分析.中国计算机学会通讯. 第十二卷第2期. 2016年2月.
6. 周明辉, 张宇霞, 谭鑫. 软件数字社会学. 中国科学信息科学. 2019. 49(11). 1399-1411.

**注解：** [1] [2] 是软件工程早期的重要文献，[1] 最早阐述了“软件工程没有通用解决方案”的核心论点，可直接Google到全文；[2] 则记录了IBM在60年代组织开发System/360操作系统的经验教训，国内有中译版，但是翻译非常生硬，推荐寻找英文PDF原版阅读；[3] 是一本软件工程入门教材，可在网上买到，和其他教材相比，内容简短易懂，行文生动有趣，非常适合作为闲暇读物；[4] [5] [6] 是关于我们实验室研究领域的概述，可以发邮件找周老师获取。

### 领域早期工作

1. Mockus, Audris, Roy T. Fielding, and James D. Herbsleb. "Two case studies of open source software development: Apache and Mozilla." *ACM Transactions on Software Engineering and Methodology (TOSEM)* 11.3 (2002): 309-346.
2. Herbsleb, James D., and Audris Mockus. "An empirical study of speed and communication in globally distributed software development." *IEEE Transactions on Software Engineering* 29.6 (2003): 481-494.
3. Mockus, Audris, and David M. Weiss. "Globalization by chunking: A quantitative approach." *IEEE Software* 18.2 (2001): 30-37.

注解：使用数据探索开源开发和全球分布式开发是本领域的开拓性工作(也是读起来有美感的论文)，需要尤其关注其研究问题和研究方法及其跟软件开发效率和质量的关系。

### 组内主要工作

#### 软件项目如何吸引和指导新人

1. Zhou, Minghui, and Audris Mockus. "Developer fluency: Achieving true mastery in software projects." *Proceedings of the eighteenth ACM SIGSOFT International Symposium on Foundations of Software Engineering*. 2010.
2. Zhou, Minghui, and Audris Mockus. "What make long term contributors: Willingness and opportunity in OSS community." *2012 34th International Conference on Software Engineering (ICSE)*. IEEE, 2012.
3. Zhou, Minghui, and Audris Mockus. "Who will stay in the floss community? modeling participant’s initial behavior." *IEEE Transactions on Software Engineering* 41.1 (2014): 82-99.
4. Tan, Xin, Minghui Zhou, and Zeyu Sun. "A first look at good first issues on GitHub." *Proceedings of the 28th ACM Joint Meeting on European Software Engineering Conference and Symposium on the Foundations of Software Engineering*. 2020.

#### Linux社区：代码提交实践和社区可扩展性

1. Zhou, Minghui, et al. "On the scalability of Linux kernel maintainers' work." *Proceedings of the 2017 11th Joint Meeting on Foundations of Software Engineering*. 2017.
2. Xu, Yulin, and Minghui Zhou. "A multi-level dataset of Linux kernel patchwork." *2018 IEEE/ACM 15th International Conference on Mining Software Repositories (MSR)*. IEEE, 2018.
3. Tan, Xin, and Minghui Zhou. "How to communicate when submitting patches: An empirical study of the linux kernel." *Proceedings of the ACM on Human-Computer Interaction* 3.CSCW (2019): 1-26.
4. Tan, Xin, and Minghui Zhou. "Scaling open source software communities: Challenges and practices of decentralization." *IEEE Software* (2020).

#### 开源项目中的公司参与

1. Zhou, Minghui, et al. "Inflow and retention in OSS communities with commercial involvement: A case study of three hybrid projects." *ACM Transactions on Software Engineering and Methodology (TOSEM)* 25.2 (2016): 1-29.
2. Zhang, Yuxia, et al. "Companies' domination in FLOSS development: An empirical study of OpenStack." *Proceedings of the 40th International Conference on Software Engineering: Companion Proceeedings*. 2018.
3. Zhang, Yuxia, et al. "Companies' participation in OSS development: An empirical study of OpenStack." *IEEE Transactions on Software Engineering* (2019).
4. Zhang, Yuxia, et al. "How do companies collaborate in open source ecosystems? An empirical study of OpenStack." *2020 IEEE/ACM 42nd International Conference on Software Engineering (ICSE)*. IEEE, 2020.

#### 软件依赖/开源供应链

1. Hao He, et al. A Multi-Metric Ranking Approach for Library Migration Recommendations. Proceedings of the 28th IEEE International Conference on Software Analysis, Evolution and Reengineering. 2021
2. He, Hao, et al. MigrationAdvisor: Recommending Library Migrations from Large-Scale Open-Source Data. ICSE 2021 Tool Demo.

## 正在进行的课题（2021.04）

1. **SE for AI**：
   1. 开发者在应用深度学习时遇到的困难？
   2. 深度学习框架的API演化情况？开发者在不同深度学习框架之间的流动情况？
   3. 不同深度学习框架的比较：技术/应用演化和未来
2. **(开源)软件供应链**：
   1. 什么因素会影响一个(深度学习)软件包的下游项目数量？
   2. 如何消解软件供应链上的安全漏洞？
   3. 相似软件包之间的迁移情况是什么样的？
   4. Dependabot等依赖管理工具的使用情况如何，有没有改进点？
3. **代码之外的软件制品**：
   1. 开发者是如何写注释的？注释是如何演化的？
   2. 新的检测代码与注释不一致的工具？
   3. 软件项目是如何组织和撰写Release Note的？
   4. 现有的Release Note生成工具的使用情况？有没有改进点？
   5. 现有代码静态分析工具的使用情况？有没有改进点？

注解：组内工作(程序员、制品及环境的关系):我们组目前的代表工作在于研究程序员、制品及环境的关系(跟组长个人意趣有关)。研究对象从个体(成熟度、学习途径、环境影响)到群体(项目最佳实践)，到生态(可持续性、可演化性)。

## 贡献者

何昊，周明辉