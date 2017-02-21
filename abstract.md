**论文摘要  （Abstract）**

We propose a direct \(feature-less\) monocular SLAM algorithm which, in contrast to current state-of-the-art regarding direct methods, allows to build large-scale, consistent maps of the environment.

**我们提出一种直接（无需特征）的单目SLAM算法，该方法与目前现有直接法相比，能够建立大规模的（large-scale），全局一致性的（consistent map）环境地图。**

Along with highly accurate pose estimation based on direct image alignment, the 3D environment is reconstructed in real-time as pose-graph of keyframes with associated semi-dense depth maps.

**（LSD-SLAM）基于直接图像配准（的方式），不仅能够得到高精度的姿态估计，而且能够实时的，基于由关键帧组成的姿态图（pose graph）所对应的半稠密深度地图，来重构3D环境。**

These are obtained by filtering over a large number of pixelwise small-baseline stereo comparisons.

**（这些深度地图的）获取是通过，在大量的像素级别上的（pixelwise），小基线（base line）立体（stereo）比较，进行滤波获得的。**

The explicitly scale-drift aware formulation allows the approach to operate on challenging sequences including large variations in scene scale.

**LSD-SLAM可以通过数学公式检测到尺度漂移（scale-drift），从而能够运行在场景尺度（scene scale）变换大的这种具有挑战性的图像序列（sequence）上。**

Major enablers are two key novelties:

**LSD-SLAM主要有两个创新点：**

\(1\) a novel direct tracking method which operates on sim\(3\), thereby explicitly detecting scale-drift, and

**\(1\) 一种新颖的基于相似变换空间sim\(3\)，运算上的直接跟踪方法（direct tracking），从而能够很明确的检测到尺度漂移，**

\(2\) an elegant probabilistic solution to include the effect of noisy depth values into tracking.

**\(2\) 使用一个优雅的概率方法，对图像跟踪过程中，来处理噪声对深度信息的影响。**

The resulting direct monocular SLAM system runs in real-time on a CPU.

**像这样的单目SLAM系统可以实时运行在一个CPU上。**

