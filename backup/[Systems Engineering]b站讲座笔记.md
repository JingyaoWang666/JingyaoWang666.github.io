### 一、什么是系统工程？
系统工程可能开始于一个模糊的概念，关注整体系统与外界交互的功能。随着下图三个团体的人不断沟通推进，逐渐细化拆分到可工程的小板块。

<img width="470" height="425" alt="Image" src="https://github.com/user-attachments/assets/545d50a6-466d-4647-86fe-15b978877b56" />

<img width="780" height="450" alt="Image" src="https://github.com/user-attachments/assets/912ee056-5ec6-413f-aa57-703725a6db3a" />

由于系统足够复杂，需要不断拆分才能到实际可行的模块。同时，需要系统架构描述、审核、权衡研究等系统工程方法。

<img width="800" height="460" alt="Image" src="https://github.com/user-attachments/assets/f907c916-21bc-49a1-98a3-82a05281e34f" />

<img width="760" height="420" alt="Image" src="https://github.com/user-attachments/assets/f06f48a4-7d27-4296-af3d-0f7a986e36ff" />




> 这一块其实有一个trade off，就是在开始前通过系统架构描述仿真、要求审核、权衡研究等系统工程方法，确保大方向正确，防止大规模的返工；同时，对于足够复杂的系统，我们也不可能在开始前就考虑到所有问题和需求，也需要先做出一个quick dirty prototype或做出一些模块，在实践中发现问题、思考创意，不断迭代优化。

例：

<img width="760" height="410" alt="Image" src="https://github.com/user-attachments/assets/b4aba52a-e8f6-4094-a2dc-f6314f341b1d" />


___


### 二、基于模型（model）的系统工程
在工程中，我们需要一系列的决策，从而整个流程形成了一个决策树。

<img width="740" height="450" alt="Image" src="https://github.com/user-attachments/assets/87dca061-bb86-4484-9410-0e712b786583" />

原则上存在一条技术路径，使得最终的结果最大化地平衡满足了stakeholder、project manager、engineers的需求。但实际工程中无法保证达到最优，我们要做的主要是通过权衡研究（trade study）尽可能选到可行的方案，之后在此基础上再迭代优化。


<img width="750" height="450" alt="Image" src="https://github.com/user-attachments/assets/0f3d2230-9b12-4277-ba8e-206edf6d340d" />

所谓权衡研究就是比较不同决策的优缺点。为了得到这些优缺点比较的信息，我们可以采取**建立模型**的方法。

<img width="700" height="458" alt="Image" src="https://github.com/user-attachments/assets/094d729e-45a5-40ba-8340-2a807ba91319" />

通过数学模型、物理模型、架构模型等，方便我们模拟功能、比较决策、探索创新等。