**引论 ** Introduction

Real-time monocular Simultaneous Localization and Mapping \(SLAM\) and 3D reconstruction have become increasingly popular research topics.

**当下，实时单目即时定位和地图构建系统（SLAM）和三维空间环境重构俨然成为学术界流行的研究课题。 **

Two major reasons are \(1\) their use in robotics, in particular to navigate unmanned aerial vehicles \(UAVs\) \[10, 8, 1\],

**这里主要有两个原因：\(1\) 这些技术广泛使用在机器人领域，特别是用于无人飞行器（UAVs）\[10, 8, 1\]的自主导航中，**

and \(2\) augmented and virtual reality applications slowly making their way into the mass-market.

** \(2\) 还有，增强和虚拟现实技术的应用正逐渐进入大众市场。**

One of the major benefits of monocular SLAM – and simultaneously one of the biggest challenges – comes with the inherent scale-ambiguity:

**单目SLAM的主要优点之一，同时也是它的一个最大挑战之一，就是它固有的尺度歧义（scale-ambiguity）这个问题：**

The scale of the world cannot be observed and drifts over time, being one of the major error sources.

**（SLAM对应的场景不同，尺度也不同，译者额外添加备注），场景的尺度，不容易被观测到，并且（单目SLAM计算过程中）随着时间（位姿估计）会产生漂移，这也是（单目SLAM）造成估计误差的主要原因之一。**

The advantage is that this allows to seamlessly switch between differently scaled environments, such as a desk environment indoors and large-scale outdoor environments.

**当然尺度歧义的优点在于，可以对不同规模大小的空间环境之间走游切换，起到无缝连接的作用，比如从室内桌面上的（小）环境和大规模的户外场景（等）。**

Scaled sensors on the other hand, such as depth or stereo cameras, have a limited range at which they can provide reliable measurements and hence do not provide this flexibility.

**另一方面，诸如深度或双目相机，这些具备深度信息的传感器（scaled sensors），它们所提供的可靠深度信息范围，是有限制的，故而不能（像单目相机那样）具有尺度灵活性（flexibility）（的特点）。**

**1.1 目前已有的单目SLAM研究成果 Related Work**

**基于特征点的方法** （Feature-Based Methods）

The fundamental idea behind feature-based approaches \(both filtering-based \[15, 19\] and keyframe-based \[15\]\) is to split the overall problem – estimating geometric information from images – into two sequential steps:

**图像特征点方法的基本思想（可以是基于滤波方式\[15,19\]和基于关键帧方式\[15\]）就是要解决从图像（帧）上估计空间的几何信息——这整一个问题，可以拆分成两个步骤：**

First, a set of feature observations is extracted from the image.

**首先，从图像中提取一组特征观测量（feature observations）。**

Second, the camera position and scene geometry is computed as a function of these feature observations only.

**其次，相机位置和场景几何信息，仅通过上述特征观测量计算获得。**

While this decoupling simplifies the overall problem, it comes with an important limitation:

**虽然这种解耦（decoupling）方法简化了（估计空间几何信息的）整个问题，但是这种方法存在一个比较大的局限性：**

Only information that conforms to the feature type can be used.

**仅仅使用了图像上符合特征类型的信息，（而图像的其他数据信息将被丢弃掉，不被使用，译者额外添加备注）**

In particular, when using keypoints, information contained in straight or curved edges– which especially in man-made environments make up a large part of the image – is discarded.

**尤其是，当使用特征点（keypoints）时，那些包含直边或曲边的图像信息——特别是构成绝大部分人造环境的，这样的图像信息，——被弃置。**

Several approaches have been made in the past to remedy this by including edge-based \[16, 6\] or even region-based \[5\] features.

**之前，已经有不少文章，提出了获取更多图像信息的方法，包括基于图像边缘特征\(edge-based\) \[16, 6\]，甚至是基于图像区域特征\(region-based\) \[5\]。**



**图片说明文字**

Fig. 1: Large-Scale Direct Monocular SLAM: LSD-SLAM generates a consistent global map, using direct image alignment and probabilistic, semi-dense depth maps instead of keypoints.



