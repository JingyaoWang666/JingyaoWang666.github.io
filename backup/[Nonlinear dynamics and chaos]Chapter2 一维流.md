<img width="490" height="105" alt="Image" src="https://github.com/user-attachments/assets/8f2d28d8-3dad-4635-a0ff-7253bd6f8822" />

### 几何的思维方式

**1.将微分方程表示成向量场**

<img width="652" height="274" alt="Image" src="https://github.com/user-attachments/assets/785a9165-fee1-4e50-8d75-32dcf4aa803e" />

比如上图的例子中，x'=0的点称为**不动点**，黑色实心点称为**稳定的**不动点，空心点称为**不稳定**的不动点。在图中的速度场中，我们可以非常轻松的回答**定性**的问题如：给定初始点x0，当t趋于无穷的时候，x趋于哪里。（趋于附近的稳定不动点）

注：还有**半稳定点**


**2.线性稳定性分析（Linearization）**

idea：在固定点（fixed point）x*处做泰勒展开，忽略超过一阶的项，得到小扰动η和f'(x*)的关系
（从应用或者说工程师的角度出发，本课程往往就假设在我们需要做泰勒展开分析的时候，函数是足够光滑的，我们不去严格的讨论光滑相关的性质是否有。）

<img width="5001022" height="325" alt="Image" src="https://github.com/user-attachments/assets/62cae6f4-1e0a-4d61-959d-c9efbe71a13b" />

<img width="490" height="210" alt="Image" src="https://github.com/user-attachments/assets/c484cdcc-2f1c-47d9-9a96-9da2718afa06" />

遇到f'(x*)=0的情况时，画出图即可。

这在一维的时候看起来是显然的，在高维中我们也会使用这个技巧。（idea：**从低维到高维**）

注：x' = f(x)解的存在和唯一性定理

<img width="1000" height="650" alt="Image" src="https://github.com/user-attachments/assets/e6fd7ff7-175d-4c33-bdeb-62ae2d9fcd84" />



**3.振动的不可能性（Impossibility of oscillations）**

<img width="600" height="230" alt="Image" src="https://github.com/user-attachments/assets/b70f7797-bef5-472c-94e0-b7d1d067bd8a" />


直观证明：如果在某点存在振动，意味着该点的速度向量是不确定的，一会儿为正一会儿为负，这与一维系统中函数f(x)的单值性矛盾。


