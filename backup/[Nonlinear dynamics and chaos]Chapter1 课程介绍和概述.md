### Logical structure of dynamics:

动力学系统主要有两类：微分方程和迭代映射（差分方程），前者是系统在连续时间的演化，后者出现在离散时间的问题中。
微分方程又包括常微分方程和偏微分方程，本课程主要关注**常微分方程**，方程中只含一个自变量——时间t

<img width="450" height="104" alt="Image" src="https://github.com/user-attachments/assets/e1eae57c-bbcd-4151-8195-c9cf17856727" />

一个系统是**线性的**，如果上述等式右边的x_i都是一次项；否则系统是**非线性的**


在这门课程中，我们不关注使用复杂函数寻求解析解，而采取：先通过一些方法得知**相空间**中**轨迹**的情况，反推解析解的情况。


<img width="500" height="600" alt="Image" src="https://github.com/user-attachments/assets/453f3d0a-c70c-4602-81a9-b3c7fd89719a" />

**非自治系统**：

<img width="460" height="600" alt="Image" src="https://github.com/user-attachments/assets/93f1c26d-debf-4f66-87de-e4f9af215592" />


总结——**本课的核心**：

<img width="500" height="260" alt="Image" src="https://github.com/user-attachments/assets/b501e6f4-a782-4019-8150-375d89fd1225" />


___

课程安排：

<img width="1000" height="440" alt="Image" src="https://github.com/user-attachments/assets/63e19002-54f2-4725-a7a4-1b2ffa46c26d" />

上图表格的纵轴是线性/非线性，横轴是相空间的维度n（也即刻画系统状态所需的变量数）。通常的大学物理会涉及第一行的线性系统，本课程维度从低到高讨论非线性系统，即上图左下角；右下角是复杂系统的部分，属于真正的科学前沿，人们还没有搞清是怎么回事；但本课程涉及的低维非线性系统基本上可以控制的不错。