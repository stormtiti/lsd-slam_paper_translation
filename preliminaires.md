**2 预备知识** Preliminaries

In this chapter we give a condensed summary of the relevant mathematical concepts and notation.

**在本章中，我们会简明扼要的给出（这篇论文）相关的数学定义和符号表示。**

In particular, we summarize the representation of 3D poses as elements of Lie-Algebras \(Sec. 2.1\),

**尤其在（2.1小节），我们会总结一下，三维空间位姿（如何）用李代数（ Lie-Algebras）的方式表达。**

derive direct image alignment as weighted least-squares minimization on Lie-manifolds \(Sec. 2.2\),

**然后（2.2小节）推导出图像直接配准法的实质，即：李群—**~~流体~~**_流形_（Lie-manifolds）上的加权最小二乘的最小化\(weighted least-squares minimization\)（优化问题）**

and briefly introduce propagation of uncertainty \(Sec. 2.3\).

**并在（2.3小节）扼要说明不确定性（协方差矩阵或叫信息矩阵，译者额外添加备注）是如何传播的。**（感谢范帝楷同学指点）

**数学符号定义** Notation.

We denote matrices by bold, capital letters $$(\textbf{R})$$ and vectors as bold, lower case letters (![](/assets/math_22.png)). _(note that: Katex doesn't support bold greek letters)_

**“矩阵” 用粗体，大写字母表示，（比如：**$$\textbf{R}$$**）， ”向量” 用粗体， 小写字母表示（比如：**![](/assets/math_22.png)**）。**

The n’th row of a matrix is denoted by $$\begin{bmatrix}\cdot\end{bmatrix}_{n}$$.

**矩阵的第n行用**$$\begin{bmatrix}\cdot\end{bmatrix}_{n}$$**来表示。（这个表达形式在3.5小节的公式18. 19中出现，译者额外添加备注）**

Images $$I : \it{\Omega} \rightarrow \mathbb{R}$$

the per-pixel inverse depth map D :  ![](/assets/math_1.png)

and the inverse depth variance map V :  ![](/assets/math_1.png) are written as functions,

where ![](/assets/math_2.png) is the set of normalized pixel coordinates, i.e., they include the intrinsic camera calibration.

**论文中提及的若干概念： **

* **图像 **$$I$$** （Image），**
* **（像素级别的）逆深度图** $$D$$ **（简称逆深度图，per-pixel inverse depth map），**
* **逆深度方差** $$V$$  **（inverse depth variance map），**

**我们用数学映射关系的函数表达如下：**

* **图像**$$I : \it{\Omega} \rightarrow \mathbb{R}$$** ，（I: 从图像向一个实数的映射）**
* **逆深度图 D :  **![](/assets/math_1.png)   **（D: 逆深度图到正实数的映射）**
* **逆深度方差 V : **![](/assets/math_1.png) **（V: 逆深度方差到正实数的映射）**

**其中： **![](/assets/math_2.png)**，Ω是归一化（normalized）的像素（二维）坐标点集合，即：包含相机内参（intrinsic）。**

Throughout the paper we use d to denote the inverse of the depth z of a point, i.e.,![](/assets/math_3.png) .

**在整篇论文中，三维空间中某一点的深度表示为z, 它的逆深度用d表示，两者的关系即：**![](/assets/math_3.png)。

