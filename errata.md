**翻译勘误表，建议和贡献者** Errata

持续更新中...

### 1. 贡献者

感谢下面各位SLAM研究者对我的启发： \(不分年龄性别，不分资历，不按照先后顺序，不管提出的问题建议大或小，轻或重，简单或深入\)

* 黄山老师 \(湘潭大学\)
* 周忠详 \(北工大\)

### 2. 问题和建议

#### 2.1 consistent的含义

google对consistent的英文解释:

> 1. acting or done in the same way over time, especially so as to be fair or accurate.
> 2. unchanging in nature, standard, or effect over time.
> 3. compatible or in agreement with something. 等等

译者认为`consistent`含义本身具有_时空上的连续性_这层含义，更具有事物在不同时间点上的一致性这个意思。比如：在进行SLAM过程中，传感器数据会随着时间的持续，计算过程中产生误差累计，发生漂移现象，这会影响相机轨迹和环境地图的一致性。

#### 2.2 refine在深度图估计中的含义

译者在深度图估计流程里面，优化当前关键帧\(refine current KF\)翻译上可能不妥，应该把`refine`翻译为**深度更新**，比泛泛的说成\[优化\]更加精确。谢谢周忠详~~

#### 2.3 concatenation operator的翻译
concatenation operator: 序连运算子，而不是~~结合律运算符~~