**翻译勘误表，建议和贡献者** Errata

持续更新中...

### 1. 贡献者

感谢下面各位SLAM研究者对我的启发： \(不分年龄性别，不分资历，不按照先后顺序，不管提出的问题建议大或小，轻或重，简单或深入\)

* 黄山老师 \(湘潭大学\)
* 周忠详 \(北工大\)
* 范帝楷 \(西工大\) 审稿
* 贺一家　审稿
* 赵搏欣（Labby）审稿
* 李月华 \(浙大\)
* 蔡育展
* 刘富强 \(引荐\)
* 张明明 \(哈工大\)
* Solomon
* 高翔博士 \(清华大学\)
* 陈创荣 \(中山大学\)
* 赵博欣老师

### 2. 问题和建议

#### 2.0 LSD 统一的翻译

Large-Scale Direct Monocular SLAM： 基于直接法的大范围单目SLAM ~~具备大规模，大尺度，基于直接法的单目SLAM~~ \(谢谢贺一家\)

#### 2.1 consistent的含义

google对consistent的英文解释:

> 1. acting or done in the same way over time, especially so as to be fair or accurate.
> 2. unchanging in nature, standard, or effect over time.
> 3. compatible or in agreement with something. 等等

译者认为`consistent`含义本身具有_时空上的连续性_这层含义，更具有事物在不同时间点上的一致性这个意思。比如：在进行SLAM过程中，传感器数据会随着时间的持续，计算过程中产生误差累计，发生漂移现象，这会影响相机轨迹和环境地图的一致性。

#### 2.2 refine在深度图估计中的含义

译者在深度图估计流程里面，优化当前关键帧\(refine current KF\)翻译上可能不妥，应该把`refine`翻译为**深度更新**，比泛泛的说成\[优化\]更加精确。谢谢周忠详~~

#### 2.3 concatenation operator的翻译

concatenation operator:  乘法（算子）~~序连运算子，而不是结合律运算符~~

#### 2.4 引论中的字词修改

谢谢范帝楷的指导

* 立体（双目）相机（stereo cameras）
* 单目SLAM，场景尺度不能被观测到

#### 2.5 收敛半径

谢谢贺一家对收敛半径的解释

#### 2.6 计算$$\mathfrak{se}(3)$$

这里计算的是当前参考帧（关键帧KF）和新图像帧（new image）之间的$$\mathfrak{se}(3)$$相对位姿变换。 谢谢张明明的讨论。

#### 2.7 残差的高度相关性话题

在2.2小节中，作者提出**残差相关性**的问题。

高度相关性作何理解？ 方差下限作何理解？ 一种观点认为残差是独立不相干的随机变量，但是实际上这些变量间是应该是相关性的，所以如果相关性的话，方差应该会更大。译者额外添加备注，还需要确认。 感谢和陈创荣的讨论。

