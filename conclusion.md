**5 总结** Conclusion

We have presented a novel direct \(feature-less\) monocular SLAM algorithm which we call LSD-SLAM, which runs in real-time on a CPU.

**我们提出了一种新颖的基于直接法的单目SLAM算法， 我们称之为LSD-SLAM，且这个单目SLAM系统,可以实时在单个CPU上运行。**

In contrast to existing direct approaches – which are all pure odometries – it maintains and tracks on a global map of the environment, which contains a pose-graph of keyframes with associated probabilistic semi-dense depth maps.

**LSD-SLAM和其它现有，仅充当视觉里程计的直接法相比，它在全局地图上进行维护和图像跟踪，这个全局地图包含由关键帧组成的姿态图，以及关键帧对应的用概率方式表现的半稠密深度图组成。**

Major components of the proposed method are two key novelties:

**我们提出的方法的主要有两个创新点：**

\(1\) a direct method to align two keyframes on $$\mathfrak{sim}(3)$$ , explicitly incorporating and detecting scale-drift

**（1）两帧关键帧之间，用** $$\mathfrak{sim}(3)$$ **直接法来配准，明确纳入和检测尺度漂移。**

and \(2\) a novel, probabilistic approach to incorporate noise on the estimated depth maps into tracking.

**并且（2）一种新颖的概率方法（这篇论文没有详细介绍深度估计，译者额外备注说明，请参考reference），将深度图的噪声（深度不确定性）融合到图像跟踪中。**

Represented as point clouds, the map gives a semi-dense and highly accurate 3D reconstruction of the environment.

**地图以点云表示，其特点是，半稠密型而且是高精度的三维环境重构。**

We experimentally showed that the approach reliably tracks and maps even challenging hand-held trajectories with a length of over 500 m,

**我们的实验表明，LSD-SLAM方法能够可靠地跟踪图像和构建地图，甚至能够成功挑战跟踪超过500米长的（手持相机图像）运动轨迹，**

in particular including large variations in scale within the same sequence \($$average$$ inverse depth of less than 20 cm to

more than 10 m\) and large rotations – demonstrating its versatility, robustness and flexibility.

**尤其是在同一图像序列中，场景尺度变化也比较大，（_平均_逆深度可以小到20厘米，大到可以超过10米）,还出现相机的大旋转运动—展示了LSD-SLAM算法的多功能性，鲁棒性和尺度的灵活性（等特点）。**

---

（完）

译者备注：

如果出现错别字,翻译流畅性问题,或者译者概念搞错,有误导之嫌,或者概念不清晰等,请麻烦告知译者,或写在译文批注里面,译者学识有限,初次翻译和学习,请赐教~~

** I'm waiting for your inspiration ~~**

**在这里再次感谢范帝楷，贺一家，赵搏欣和蔡育展等各位老师同学的审稿和纠正**
