# 先置知识

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
