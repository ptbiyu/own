---
title: 敏捷之Log Work和燃尽图
tags:
  - 'Log Work,燃尽图'
categories:
  - PM
abbrlink: a76b2518
date: 2017-07-24 12:19:08
---

## Log Work 
Log Work 记录工作日志，敏捷开发中项目管理的时间管理方式。每天上班或者每天下班记录一下前一天或者当天的工作耗时。

那么Log Work到底是在做什么：
1. 每天重新评估你正在做的项目需求（强制，团队的统一标准）
2. 梳理一下你今天做的事情都有什么
3. 给项目经理看数据，把控项目进度，长期来看最终的提升是落实到个人身上的，梳理工作效率，提高效率的收获在个人  

一天，一个版本的Log Work也许产生不了太大的效果，反而觉得耗时，但是长久下来的数据积累将对项目管理产生重大的帮助，是敏捷开发的数据量化方式之一。  Log Work的数据产出燃尽图。
## 燃尽图
>燃尽图（burn down chart）是在项目完成之前，对需要完成的工作的一种可视化表示。燃尽图有一个Y轴（工作）和X轴（时间）。理想情况下，该图表是一个向下的曲线，随着剩余工作的完成，“烧尽”至零。燃尽图向项目组成员和企业主提供工作进展的一个公共视图。  
>
>
>

1. 横轴表示时间，体现的是完成工作所需的时间；
2. 纵轴表示未完成的工作量；
3. 标准曲线，假定成员工作生产率恒定情况下的进展曲线；
4. 实际耗费曲线：实际进展曲线，实际花费的时间；
5. 实际剩余曲线：实际剩余时间，团队成员所有任务的剩余时间的总和；
    
随着工作的进行时间的推移，纵轴的工作量在逐渐减少，实际剩余曲线虽然与标准曲线有一定差距，但燃尽图总体趋势就是逐渐向下最后燃烧至尽。

一个迭代的燃尽图没什么意义，持续迭代的燃尽图可以用于一些分析或数据积累，但它不是用于承载绩效考核等管理手段的工具。

一张理想的燃尽图，剩余时间应该贴近标准线上下浮动
![image](/images/1500987658768.jpg)


***

## 案例分析  
最早的时候部门以人天估算，没有进行Log Work，kanban的工作流从开发完成后进入测试阶段就一直没有状态改变直到测试完成，燃尽图的状态就会呈现一直不动的状态，对项目管理起到的作用就很小，从而重新规划kankan，去掉了测试中和测试完成的步骤，开发完成就代表这个需求完成了,并且引进了Log Work的工作流。

![image](/images/1501028844618.png)
![image](/images/1501030158470.png)
改进后的kanban
![image](/images/1501029011058.png)
下面以我们部门的Log Work方式和燃尽图数据作为一个案例分析(使用JIRA作为项目管理工具，以人时估时)
<div align=center>
     ![image](/images/1500996744538.png)
</div>              
上图是一个原本预估需要6个小时完成的需求，在7月21号log work过一次，当天开发了3个小时那么剩余预估时间还剩3个小时，今天又一次Log work了3个小时，如果在没有调整剩余工作量的情况下那么这个需求开发完成了，如果手动调整了剩余时间不为0，说明这个需求开发了6个小时还不能完成，那么需要结合情况总结是预估时间过短了，还是中间依赖项delay导致的情况，或者其他依赖项原因造成。

最后所有人所有需求的Log  Work 最后可以产出这个迭代的燃尽图：
首先分析Android的燃尽图
![image](/images/1500996894578.png)
<div align=center>红线代表剩余时间，绿线代表消耗时间，灰色代表标准曲线</div>
看到图的时候我们可以直观看到一些问题：
1. 头3天红线一直往上走，是需求变更吗？
2. 正常情况红线应该消耗到0，为什么没有？
3. 理想情况绿线和红色是对称的，开发后期的曲线显示的确如此，我们第一次做Log Work的就能得到这么完美的数据，是否存在造假？  

贴一张Log Work的日志  
![image](/images/1500999179826.png)


后面团队一起分析：
1. 头三天在等待团队另一个成员的到来，所以需求拆分后没有估时分配，那么在这块的优化就可以提高，每个版本的需求不应该被拆分了好几天，讨论需求分配任务时间太久，要降低，另外提前开下一个版本的需评会也可改善这个问题
2. 红线没有消耗到0，其中一个商业化需求被移走了，所以无法被消耗掉
3. 我们的预估每个人一天有6个小时的工作时间，其实这是一个就当时定的时候相对较高的时间，现在走的这么准，那么一天真的有6个小时的有效工作时间？后期请要求团队成员客观真实的进行Log Work，数据太理想，我们怎么进行校准，我们的目标不是数据完全准，而是越来越准


然后来看下这个迭代iOS的燃尽图
![image](/images/1500997075536.png)
1. 绿线按理至少要到红线的最顶端，结果没有，那是你们的预估有问题还是效率高？
2. 头几天需求一直上升是为什么？

团队分析：
1. 有人一直在变更需求，直接编辑需求，拆解子任务，拆解任务和Log Work不冲突，拆解子任务主任务要清0
2. 燃尽图怎么筛选出个人的

项目组成员的总体情况有：
1. 有人不知道怎么Log Work
   * 我根本不知道今天对这个需求工作了多久（这里面一定有提升空间，慢慢养成习惯记录，不应该在凭感觉，项目的把控能理会越来越好）
   * 要不要把code review的时间算在这个需求里面
   * 开会，上厕所的时间要不要去掉（统一标准就好）
2. 不要有编辑需求的操作，会导致Log日志RTE改变（需求变更的意思），所有的工作都通过Log Work记录，误操作可以删除记录日志
3. 如果需求预估时间太低，在Log Work的时候修改剩余时间，后续可以判断类似需求的大概预估量了
4. 我们在预估需求的时候要不要把提测之前修改bug的时间预估上，不然的话一个人有多个任务的时候修改bug会占用掉开发下一个任务的时间，那么要不要呢？最后团队内部讨论->要，那么修改bug的时间是多少呢？多少比例？大家一起讨论了一个10%（提高团队成员的积极性），先试行一下，不准也可以，我们要的是越来越准，通过控制这个时间，提高了我们的代码质量，bug越来越少
5. 每个需求的讨论沟通要不要预估，要不要Log Work，讨论—>要，其实沟通涉及到工作人不少，和第三方sdk的对接等等都相对耗时，我们要记录的不是写代码的时间，是整个需求完成的时间，假设一个类似的需求从讨论到完成要10个小时，讨论了6个小时，那么现在评估4个小时就不合理，需要的在了解讨论过程碰到的问题，从而改进流程
6. 另外需求涉及到的依赖项如UI也要评估时间，对依赖项的不可控一段时间之后就可以看出对团队的影响有多大，改善流程，看依赖项能不能提前准备
7. 红色和绿线对不上的时候，如果红色比绿线高，那么一天的工作时长小于6个小时，如果红色比绿线低，那么一天的工作时长高于6个小时，然后调整自己的工作时间，得出团队的平均生产率，5个小时？7个小时？

## 总结
1. PM看燃尽图完美不代表项目没有问题，等燃尽图一直处于没有下降状态，发现问题有时就会太晚了
2. 燃尽图跟进不到依赖项
3. 燃尽图看不出项目排期问题，排期要借助甘特图（项目进度网络图）
4. 燃尽图容易看出估时和需求变更的问题
5. 燃尽图不应该作为项目绩效的考核，我们要做真实的Log Work记录，通过工具和方法得出结论，真实客观数据拆解出问题的根本，得出一套解决方案，提高团队的生产率
6. 目的不是为了一开始就很准确的数据，而是越来越准确的数据，评估越来越准，根据数据可以梳理出一个需求的量级（大，中，小），受到哪些影响（沟通细节，依赖项，产品细节等等），然后拆解
7. 有人提出要看个人燃尽图，推荐JIRA插件Tempo，工时管理，时间计划和跟踪变得轻松简便


