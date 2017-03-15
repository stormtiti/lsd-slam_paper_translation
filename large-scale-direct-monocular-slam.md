**3 **~~**具备大规模，大尺度，基于直接法的单目SLAM**~~ **基于直接法的大范围单目SLAM** Large-Scale Direct Monocular SLAM

We start by giving an overview of the complete algorithm in Sec. 3.1, and briefly introduce the representation for the global map in Sec. 3.2.

**3.1小节，我们首先给出整个LSD-SLAM算法的大概述，然后在3.2小节，我们简单介绍LSD-SLAM**~~**所用到的地图**~~**是如何表示地图的（数学模型）。**

The three main components of the algorithm are then described in

Sec. 3.3 \(tracking of new frames\),

Sec. 3.4 \(depth map estimation\),

Sec. 3.5 \(keyframe-to-keyframe tracking\) and

finally Sec. 3.6 \(map optimization\).

**LSD-SLAM算法的三个主要模块，将在如下小节进行详解：**

* **3.3小节 新图像的跟踪 \(具体来说，就是当有新的图像输入时，它与当前关键帧之间se\(3\)的变换关系，译者额外添加备注\)**
* **3.4小节 深度图估计**
* **3.5小节 关键帧之间的跟踪，（具体来说，计算关键帧之间的sim\(3\)，译者额外添加备注）**
* **3.6小节 地图优化**



