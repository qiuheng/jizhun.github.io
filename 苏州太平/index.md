# 苏州·太平金融中心BIM实施

## 项目介绍

案例是一个异形、双曲面的玻璃屋盖幕墙系统。

![img](https://pic3.zhimg.com/80/v2-694b7a1a3a43e5992ad0608c9411dcec_720w.jpg?source=d16d100b)

如效果图所示，玻璃屋盖呈波浪状，塔楼装饰条与屋盖装饰条需要无缝连接。  看似随意任性的造型，产生了一系列难题：

![img](https://pic1.zhimg.com/80/v2-e5d1b20d9330a9bfd1a4797858afa19e_720w.jpg?source=d16d100b)



难点1，由于分格玻璃板块尺寸全都不同，放置方向各异，对准确的建模带来了很大的难度，尤其是在还未考虑周全的节点系统条件下，完成各种铝材，钢材的的建模。

![img](https://pic1.zhimg.com/80/v2-363273c28ae016e52f995e436a677152_720w.jpg?source=d16d100b)



难点2，装饰条从塔楼西立面扭转过渡到南立面，如何能同时保证拼接效果与施工可行性。

![img](https://pic2.zhimg.com/80/v2-4e6e36063c5f0028911ee40f43253576_720w.jpg?source=d16d100b)



难点3，钢结构梁宽度仅为150mm，且法向任意，钢结构的水平施工误差对于面板支撑钢件的生根定位支持很差。

## 曲面幕墙的平板化

![img](https://pic1.zhimg.com/80/v2-93d50f20e992300b258431caf4ab1a53_720w.jpg?source=d16d100b)



以50的阶差为界限，预览造型扭曲的分布。

![img](https://pica.zhimg.com/80/v2-96d717f64b0521ab7cf7112109c55086_720w.jpg?source=d16d100b)

采用提取3点所在平面。第四点投影至该平面的方式，把曲面分格用平板玻璃替换

![img](https://pic2.zhimg.com/80/v2-ee16cbc9c9bf269825e0afae0e86870b_720w.png?source=d16d100b)



由于曲度走向的渐变，会出现直板的第四点有时是凹陷点（低于原曲面）的情况，这时要进行筛选，并更换东北点为西北点来作第四点，以保证第四点都为翘起点而非凹陷点。   

## 小样板设计 (冷弯与翘边对比)

小样板用4块玻璃做冷弯曲板，4块做翘边直板。来实现对比——

![img](https://pic1.zhimg.com/80/v2-1f842604853eab2f97551eb69197857b_720w.jpg?source=d16d100b)



翘边做法的效果没有横向压板的存在，获得了设计的认可。

![img](https://pica.zhimg.com/80/v2-e07696ea9b2393a71d4e2555d1e24206_720w.jpg?source=d16d100b)



![img](https://pic2.zhimg.com/80/v2-dcd39e8294f8d48ccbacaa09f2261c33_720w.jpg?source=d16d100b)



BIM模型效果实际现场效果 最终确认屋盖全部采用翘边平板的做法。 
## 视觉样板设计
视觉样板做了30片玻璃，发现了问题——

![img](https://pica.zhimg.com/80/v2-4aca3eaf11ed115609d7760583106102_720w.jpg?source=d16d100b)



  

  

相邻玻璃板块公用型材，所以玻璃和型材之间必然存在非90度的特殊夹角。

![img](https://pic3.zhimg.com/80/v2-c971fa9431b0a4ec0a07ed6a85edfedf_720w.jpg?source=d16d100b)



  

  

为使玻璃安装至正确位置，铝折板副框需呈无规则梯形定制。

![img](https://pic1.zhimg.com/80/v2-941a7c768206a8c91d7317a7ce4fa0aa_720w.jpg?source=d16d100b)



  

  

这给设计和工厂都出了难题，我使用grasshopper批量完成了梯形折板的出图，但对于加工厂那边仍然十分困难了。   经过视觉样板的测试后，最终将系统优化为半单元式，取消了公用型材，改为相邻玻璃各自使用自己的型材。
## 装饰条方案设计
装饰条的造型效果一直是业主和设计关注的重点，装饰条效果的实现有如下2个难题：  （1）剪刀误差

![img](https://pic2.zhimg.com/80/v2-060026ae789e0eae66664c33038dd413_720w.jpg?source=d16d100b)



  

  

当流线为空间曲线，两个相邻长直物体，放置方向角成一定角度，并用公共平面斜切密拼的情况下，交界处会像打开的剪刀一样错位。剪刀的交叉点为长直物体的定位基点。想了解更多关于剪刀现象，请参考这里-->[小知识| 异形线材建模中的剪刀现象](http://mp.weixin.qq.com/s?__biz=MzU2NTU4Nzk1MA==&mid=2247483889&idx=1&sn=0bae06eeb4cfddbd6fbe3574e295e868&chksm=fcb83b70cbcfb2662fb4abe7476d8e05e02537c6d93e6f5f60e464b3cc793967973cda9eb6bc&scene=21#wechat_redirect)  剪刀现象带来的错位效果是不可避免的，并且会让流线性效果大打折扣。通过BIM建模的过程中对这一问题的探究，找到了这样的优化方法：

![img](https://pic1.zhimg.com/80/v2-dad3084f50d68f96ae582c2233ffe5c8_720w.jpg?source=d16d100b)



  

  

最终系统的设计因此建议得以改进，装饰条的做法从270mm高改为150mm高，从玻璃分格缝定位优化为在装饰条顶部向下75mm处设中轴定位。拼接效果的到了明显改善。 原装饰条定位基点在型材支点处新基点在装饰条顶下75mm的轴处

![img](https://pic1.zhimg.com/80/v2-3b12177efe45c1da680f0bed844e60c4_720w.png?source=d16d100b)



  

  

![img](https://pic1.zhimg.com/80/v2-63f6d5cfa17e30431df659961dc62699_720w.jpg?source=d16d100b)



  

  

装饰条基线重定位 最终的剪刀偏差变得很小  （2）错台偏差

![img](https://pica.zhimg.com/80/v2-8a02e1f7eaf0523729c11814453edf63_720w.png?source=d16d100b)



  

  

装饰条的设计中还存在着一个错台偏差的问题。 因为玻璃面板呈翘边状，装饰条与玻璃间隙存在着不均等错台。为使错台间隙趋于一致，设计方提出以翘曲点向上偏移一定距离，作为装饰条下口定位基线。而装饰条的效果存在着衔接渐变，所以偏移值在与塔楼衔接段和收尾段有所差异。 rhino进行方案的推演过程

![img](https://pic1.zhimg.com/80/v2-84e30284cc4dfc0bc1033a43042c6e89_720w.png?source=d16d100b)



  

  

1.连接翘曲玻璃最高点多段线a

![img](https://pica.zhimg.com/80/v2-1d7114bdc77daf086f032646689dba7e_720w.png?source=d16d100b)



  

  

2.将原始曲面玻璃对应点位向玻璃法线方向向下偏移一定距离，连接成多段线b

![img](https://pic1.zhimg.com/80/v2-7a655dde2d89de480c961315d54ee0b1_720w.png?source=d16d100b)



  

  

3.将a的每一个端点沿b的每个对应端点与之连线的方向根据渐变情况做不同的偏移距离，并连接成多段线c

![img](https://pic1.zhimg.com/80/v2-85b3148065c347f17020907a1f5b4329_720w.png?source=d16d100b)



  

  

4.前7个点依次偏移225mm，225mm，225mm，225mm，185mm,145mm,105mm

![img](https://pica.zhimg.com/80/v2-937a12a9bd4c63d719aa81f4641ec926_720w.jpg?source=d16d100b)



  

  

5.中间的所有点——105mm，后四个点依次偏移105、85、65、45mm

![img](https://pic2.zhimg.com/80/v2-e6541655c30794cf7221d53ab2d5dc68_720w.jpg?source=d16d100b)



  

  

6.根据c和b的每个线段所成平面放置装饰条，前六段采用270mm高度截面，剩余的采用150mm高度截面

![img](https://pica.zhimg.com/80/v2-a3bc8bcf70e43ad66126635001bb0ac6_720w.jpg?source=d16d100b)



  

  

7.根据玻璃原始完成面向上偏移30mm为切面切除各过渡段装饰条下口，完成最终模型。  ‍2 材料下单 **2.1** **面材下单的运用** 2.1.1彩釉玻璃 彩釉点数量大，对于深化设计师CAD制图而言，完成1700块玻璃上彩釉点的出图要耗时两个月之久。

![img](https://pic2.zhimg.com/80/v2-61f5fc784c09b963a03493af43df4577_720w.jpg?source=d16d100b)



  

  

通过参数化程序排布玻璃彩釉点，连同每块玻璃的加工尺寸一起表达为预加工图。则大大减少了工作时间。  2.1.2铝板

![img](https://pic3.zhimg.com/80/v2-38cc421e15ec317a25529f550428e5b6_720w.jpg?source=d16d100b)



  

  

对于四边形铝板，对接的铝板加工厂可以根据数据表格来加工，通过grasshopper将Rhino模型的板块数据提取处理。数据输出表格的技巧参考这里-->[小技巧|grasshopper与Exel/wps的复制粘贴交互](http://mp.weixin.qq.com/s?__biz=MzU2NTU4Nzk1MA==&mid=2247484119&idx=1&sn=eaec7c0b939d4d371f703d545c2cc80f&chksm=fcb83856cbcfb140b286b76b85757aee33a4fc76b4e113473fad5926a93d5c32da531ac3fa1b&scene=21#wechat_redirect) **2.2** **线材下单的运用** 2.2.1装饰条 装饰条加工图的难点在于三维切角的表达，在屋盖首尾区域共9排的渐变区装饰条，还存在着侧面和底面各切一刀空间斜角的情况。

![img](https://pica.zhimg.com/80/v2-47859816c7e3cb4d6eb5f716eec797e4_720w.jpg?source=d16d100b)



  

  

与塔楼衔接处6段渐变

![img](https://pica.zhimg.com/80/v2-6bc143a8689bcffb1e9028de2febf607_720w.jpg?source=d16d100b)



  

  

尾部3段渐变

![img](https://pic1.zhimg.com/80/v2-f467e895a0e1830cb6e0a6003b604b1b_720w.png?source=d16d100b)



  

  

批量输出的预加工图对于有切角的型材批量建模与出图，实现更加麻烦，需要一定的技巧，暂不赘述。 2.2.2玻璃护边

![img](https://pic2.zhimg.com/80/v2-035b0b9b6ccda5649ebbfaa8be27ae7c_720w.jpg?source=d16d100b)



  

  

批量输出预加工图 玻璃互边与玻璃面板存在平面上的推导关系，但由于玻璃敲边阶差的存在，在护边的高度上有所差异，因此在grasshopper程序中要将翘值参数结构化的传递过来。  2.2.3月牙铝包边板

![img](https://pic1.zhimg.com/80/v2-4b7b90c26a52c7b1dfd96b0f9b705451_720w.jpg?source=d16d100b)



  

  

包边铝板与装饰条相似，都存在剪刀误差，也存在三维拼切角，因此加工图的表达上需要有切割数据。

## 钢件下单的运用

根据适用分类条件，进行筛选得以统一下单的钢件数量

![img](https://pic3.zhimg.com/80/v2-fc2e1bb7adc9ee947f51499dab6e207d_720w.jpg?source=d16d100b)



  

  

主钢件优化为8种

![img](https://pic1.zhimg.com/80/v2-1ee699f00307d14a1e33486de5c2051c_720w.jpg?source=d16d100b)



  

  

次钢件优化为3种 同样由于玻璃翘边的存在，钢件的长度也不尽相同，全部统一做的最长又容易浪费材料，所以根据20mm的阈值，进行了钢件种类优化。 3 指导施工 

## 三维扫描结果的检查

![img](https://pica.zhimg.com/80/v2-746c021b786769db45466a71e5ff9d4f_720w.jpg?source=d16d100b)



  

  

 

![img](https://pica.zhimg.com/80/v2-e399cd0acebd27fc7aa993d657c1384b_720w.jpg?source=d16d100b)



  

  

扫描现场和理论模型进行对比

![img](https://pic3.zhimg.com/80/v2-0a79e699a3533c149528cc7b20f27c87_720w.jpg?source=d16d100b)



  

  

钢梁误差位置分布，红色区为不满足安装空间位置。

![img](https://pic2.zhimg.com/80/v2-966dc3b99d6bee2517e6f92039b8ed8e_720w.jpg?source=d16d100b)



  

  

垂直误差数据列表，负值表示不满足150mm安装空间的距离。   最大误差86mm，说明钢梁在此处实际高于理论值86mm，按理论表皮下单则我们的幕墙无法按理论位置安装

![img](https://pic3.zhimg.com/80/v2-2a847cc863215a135d5202c792fd0cf1_720w.jpg?source=d16d100b)



  

  

水平方向误差图示   水平误差的存在，会使幕墙型材的支撑钢件落于钢梁边缘甚至钢梁之外。给定位和安装带来巨大不便的同时，还会人在屋架之下影响仰视的效果。  

## 钢结构梁施工误差的解决
BIM设计师提供两种方案供业主选择——

![img](https://pic1.zhimg.com/80/v2-4a70c9a25c0403a77be0a3238f608a3f_720w.jpg?source=d16d100b)



  

  

![img](https://pica.zhimg.com/80/v2-fde8eb4ee5ff3992577d14a0e776ada5_720w.png?source=d16d100b)



  

  

方案一整体抬高方案二调整所有表皮偏差的点位

![img](https://pica.zhimg.com/80/v2-3d64b8c78ae61ec03e943ab12f6fe17c_720w.jpg?source=d16d100b)



  

  

![img](https://pic1.zhimg.com/80/v2-cf9faef6b9ca641a829f6294aaceb7c8_720w.jpg?source=d16d100b)



  

  

方案一调整后的表皮模型方案二调整后的表皮模型 表皮调整方案一：理论模型整体向外偏移抬高，偏移值以满足最小安装间距86mm为准。 表皮调整方案二：根据结构调整表皮，根据三维扫描点数据，提取钢梁中的位置向法线之上推出表皮。 最终，重构表皮的方案二，赢得了项目部、业主和设计的一致认可。 这也是最能体现BIM价值的一环，将三维激光扫描现场与参数化设计技术结合，以“因地制宜”的方式，定制了最终的幕墙产品形态。 根据新确认的表皮，利用先前写好的grasshopper程序更新了所有材料模型，用于后续大规模下料。 

## 测量放线数据的输出
屋盖的所有面材和线材都是定制化的加工，所以，幕墙安装的定位点也必须精准。为了保证安装的精确，BIM设计师提供的点位必须准确。

![img](https://pic3.zhimg.com/80/v2-87f68b1fe4bc54ec9db84c96fcd46fab_720w.jpg?source=d16d100b)



  

  

提供空间定位编号模型，供放线员理解。每个钢件放线三个点，a和b为外侧面上口端点，c为外侧面中心点

![img](https://pica.zhimg.com/80/v2-ed9fbd305b768650a514e88c68d86282_720w.jpg?source=d16d100b)



  

  

提供CSV数据表，三维坐标与编号对照。  **3.4** **全站仪放线路径的对接与按需定制**

![img](https://pica.zhimg.com/80/v2-18e6704ba19b4d71c446f36589b1402b_720w.png?source=d16d100b)



  

  

![img](https://pica.zhimg.com/80/v2-9d8384d67908d7f504be65789adbb2b5_720w.jpg?source=d16d100b)



  

  

由于测量员的放线需求是延次梁一排排的顺序过去，需要同一梁上两个钢件测量点紧挨着排序，再到同一列的下根钢梁，这列钢梁结束，再到第二列钢梁按同样的顺序排布。  通过grasshopper程序的数据筛选处理能力，协助放线员减轻了表格处理的工作，生成符合放线路径的坐标表
## 实际施工
先放线并在现场定出钢件上端控制线

![img](https://pic2.zhimg.com/80/v2-ad04bee96df8c2f7691b07f65d95cc6c_720w.jpg?source=d16d100b)



  

  

再根据控制线辅助下装好钢件位置

![img](https://pic3.zhimg.com/80/v2-dc95c6c688c0912110e42e040acce7a2_720w.jpg?source=d16d100b)



  

  

再装工厂加工好的玻璃单元

![img](https://pic4.zhimg.com/80/v2-8e7b29b1c92d0f882bf8ecfcca9d60e5_720w.jpg?source=d16d100b)



  

  

## 经验总结
双曲波浪造型的玻璃屋面，具有很大的工程难度。本项目借助参数化设计技术解决了诸多前所未有的问题。尤其是在幕墙系统的三次改进、返尺重建表皮、装饰条的建模与加工、放线的指导等阶段上，发挥了巨大的作用。 **有别于很多常规幕墙项目上的BIM应用，让设计从理论上可实现、让施工在实践中可落地，是本项目BIM工作的最大亮点。** 我也希望BIM技术能在未来更加朝向物尽其用、指导施工的方向发展。



  

  

