**论文摘要  （Abstract）**

We propose a direct \(feature-less\) monocular SLAM algorithm which, in contrast to current state-of-the-art regarding direct methods, allows to build large-scale, consistent maps of the environment.

我们提出一种~~直接（无需特征）的单目SLAM算法~~_基于直接法的单目SLAM算法_，该方法与目前现有直接法相比，能够~~建立~~_构建_~~_（大规模），_~~大尺度的（large-scale），全局一致性的（consistent map）环境地图。

改动\_Labby：删除"大规模"。

> **Note** Patrick交叉审稿: large-scale是大尺度的含义，我偏向范帝楷的修改，改成大范围，以上是我的拙见，请指教。

---

**我们提出一种基于直接法的单目SLAM算法，该方法与目前现有直接法相比，能够构建大范围(large-scale)，全局一致性的（consistent map）环境地图。**

---

Along with highly accurate pose estimation based on direct image alignment, the 3D environment is reconstructed in real-time as pose-graph of keyframes with associated semi-dense depth maps.

~~（LSD-SLAM）基于直接法图像配准（的方式），不仅能够得到高精度的姿态估计，而且能够实时，基于由关键帧组成的姿态图（pose graph）和对应的半稠密深度图（semi-dense depth map），来重构三维环境。~~

（我们的方法）不仅能够基于直接图像配准（direct image alignment）得到高度准确的姿态估计，而且还能够进行在线（real-time）三维环境重构，重构的（点云）地图是由姿态图（pose graph）上的关键帧对应的半稠密深度图（semi-dense depth map）（~~叠加~~融合）组成。(谢谢蔡育展老师指教，确是，融合里面包换机械式的叠加，译者额外添加备注)

改动\_Labby：（我们的方法）除了能够基于直接图像配准（direct image alignment）得到高度准确的姿态估计外，还能够将三维环境地图实时重构为关键帧的姿态图和对应的半稠密的深度图。

> **Note** Patrick交叉审稿: 重构为关键帧的姿态图和对应的半稠密的深度图，翻译没有问题，但是初学者可能不好理解，略微具化一点，谢谢赵博欣老师，蔡育展老师提出的'融合'比我的'叠加'，翻译更加精确。以上是我的拙见，请指教。我翻译的有点啰嗦。

---

**(我们的方法)除了能够基于直接图像配准(direct image alignment)得到高度准确的姿态估计外，还能够进行在线(real-time)三维环境重构，重构的(点云)地图是由姿态图(pose graph)上的关键帧对应的半稠密深度图(semi-dense depth map)融合组成。**

---

These are obtained by filtering over a large number of pixelwise small-baseline stereo comparisons.

~~（上述姿态图和深度图）是基于图像像素级别（pixelwise），大量小基线（base line）三维立体模型（stereo）比较，筛选计算得到。~~

（相机轨迹和点云地图，译者额外添加备注）这些结果，是通过滤波方式计算得到，这个方式要使用到大量像素，小基线的立体~~比较~~配准。

改动\_Labby：这些都是通过对大量像素点对之间的基线立体配准结果滤波后得到的。

> **Note** Patrick交叉审稿: 这里强调像素小基线立体配准的滤波方式。

---

**(相机轨迹和半稠密地图)这些都是通过对大量像素小基线立体配准的滤波方式得到的。**

---

The explicitly scale-drift aware formulation allows the approach to operate on challenging sequences including large variations in scene scale.

**LSD-SLAM可以通过（我们选择的）数学公式，计算尺度漂移（scale-drift），从而能够运行在难度比较大的图像序列（sequence）上，诸如：场景尺度（scene scale）变换比较大的场合。**

改动\_Labby：算法提出了计算尺度漂移的公式，即便是当图像序列的场景尺度变化较大时也能够适用。

Major enablers are two key novelties:

**LSD-SLAM主要有两个创新点：**

\(1\) a novel direct tracking method which operates on $$\mathfrak{sim}(3)$$, thereby explicitly detecting scale-drift, and

**\(1\) 一种新颖的基于（相似变换空间对应的李代数）**$$\mathfrak{sim}(3)$$**上的直接跟踪法（direct tracking），从而能够很明确的检测到尺度漂移，**

\(2\) an elegant probabilistic solution to include the effect of noisy depth values into tracking.

\(2\) 使用一种~~优雅的简练的~~概率方法，对图像跟踪过程中，处理噪声对深度图像信息的影响。

**\(2\) 提出一种新的基于概率模型的深度噪声处理方法**(译者：谢谢蔡育展老师指导)

The resulting direct monocular SLAM system runs in real-time on a CPU.

~~像这样的单目SLAM系统可以实时运行在一个CPU上~~。 （译者： 谢谢SLAM研究群 黄老师帮助）

_**这个单目SLAM系统，可以实时在单个CPU上运行。**_

改动\_Labby：最终结果证明直接单目SLAM算法能够在CPU上实时运行。

