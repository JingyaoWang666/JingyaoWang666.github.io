### 一、评估（Evals）
在优化系统时需要一个评估系统来指示系统表现。下图展示了评估的四个象限：有无标签 + 主/客观

<img width="1200" height="660" alt="Image" src="https://github.com/user-attachments/assets/c88317f4-0e50-4013-a14b-721efa03abc4" />


一个重要的工程tip：**先建立快速粗糙的原型，再迭代优化！**
很多时候，这比把试图把一切先考虑周全再开始做要高效很多。利用观察结果来确定后续开发工作的优先级和方向，避免脱离实际过度空想。


<img width="1200" height="600" alt="Image" src="https://github.com/user-attachments/assets/fe933921-6c0e-41fb-a105-de320eb2c0c6" />

___

### 二、错误分析与确定后续步骤优先级（Error Analysis）
当系统复杂起来后，系统、科学的错误分析显得尤为重要。在上面的一中我们谈到的主要是end to end evals，但当系统的输出不理想时，工作流程中的每一步（span），或者说整条trace都有可能导致这个结果。
与其凭直觉选择一个模块进行优化，优化很久后发现对系统表现没有帮助，不如采取科学的错误分析方法。

<img width="800" height="450" alt="Image" src="https://github.com/user-attachments/assets/772403b1-fcd6-4174-9902-ef0353af267e" />

**Idea**：“解工作链”，让人类专家看每一步的输出（span）是否低于人类水平？
例：

<img width="800" height="430" alt="Image" src="https://github.com/user-attachments/assets/1a3053e3-272a-43a4-a06e-8e444d8e61d5" />

对应不同的prompt，可能有的输出没问题，有的输出有问题。上图中Prof. Andrew Ng给出的**表格法**能够清晰地反应不同模块出问题（低于人类表现）的频率，从而更加科学高效地指示值得以更高优先级优化的模块。（因为在一个复杂系统中，有太多的方面或模块可以优化，科学的工作应当有工作重心的优先级排序）
所以，error analysis也可以看作是模块级（component level）的evals，或者说指导了应当着重优化哪一个板块。


<img width="740" height="300" alt="Image" src="https://github.com/user-attachments/assets/c7f3e7c3-8d9c-49bc-a0ad-0dd578d7de31" />


> 其实上面谈到的评估evals、错误分析error analysis，不仅仅是agentic workflow，我们自己的工作系统也是同样适用！


___


### 三、组件级评估 (Component-Level Evals)

在二中我们谈到，使用error analysis指导哪一个板块需要着重优化。对于特定板块，我们会考虑建立组件级评估。
比如对于网页搜索引擎，我们尝试更换不同的网页搜索引擎，可以用信息检索领域的标准指标（如 F1 分数），编写代码来衡量网页搜索的输出列表与黄金标准列表之间的重叠程度


<img width="650" height="230" alt="Image" src="https://github.com/user-attachments/assets/2b1fc2f5-115c-4bf3-a67d-6a482b9134db" />


> 组件级评估与端到端评估的关系与顺序如下：
> 
> 1. 通过错误分析确定一个问题组件（如网页搜索）。
> 2. 构建和使用组件级评估来高效地进行调优和增量改进。
> 3. 在调优后，运行最终的端到端评估，以验证组件的改进确实提升了整个系统的整体性能。


___

### 四、怎么解决发现的问题？How to address problems you identify?

<img width="750" height="430" alt="Image" src="https://github.com/user-attachments/assets/7c7244a6-03da-4c4e-8726-70bff3884ede" />


<img width="700" height="350" alt="Image" src="https://github.com/user-attachments/assets/9cc13a55-ca0a-47f0-b90b-53c6b455cef7" />



不同的LLM模型有不同的能力和擅长。拥有对不同 LLM 能力的直觉，能使开发者更高效地选择模型和编写提示词。这样的直觉要如何培养？


<img width="750" height="300" alt="Image" src="https://github.com/user-attachments/assets/7c935fed-596c-46c6-bd6c-a6fe4a0ed5c8" />


___


### 五、延迟和成本优化优化（ Latency, cost optimization ）

在系统输出质量达到要求后，下一个优化重点是：优化工作流程的延迟和成本。
需要强调的是，对于早期团队而言，高质量的输出是首要关注的问题。系统运行良好后，才考虑将精力转向延迟或成本优化。

延迟或成本优化时，我们都看整个trace每一步花的延迟或成本，从而指导我们应当将精力花到哪一个模块上，而哪一个模块对系统提升不大。（对于系统工程，这是我们始终要做的：合理分配工作重心和优先级）

<img width="800" height="435" alt="Image" src="https://github.com/user-attachments/assets/8fa6c54d-363e-40e5-91e3-547295f79c71" />


<img width="650" height="285" alt="Image" src="https://github.com/user-attachments/assets/84863622-0d37-470a-9aad-978a72ebdf84" />



___


### 六、总结

<img width="800" height="440" alt="Image" src="https://github.com/user-attachments/assets/2f23228d-ba88-4d90-ad49-0bcb8d6da1b6" />


<img width="750" height="300" alt="Image" src="https://github.com/user-attachments/assets/b584f20d-5199-4d82-ae0f-46b90f14cd83" />


缺乏经验的团队往往花太多时间在构建上，少得多的时间用于分析和评估。而Prof. Andrew Ng指出，构建agentic workflow（或其他任何系统工程）应当是在构建和分析中不断切换，**用科学的analysis去指导build迭代优化的重心**。


一个小tip：在早期，市面上有许多工具可以帮助监控追踪、记录运行时、计算成本等。团队可以尽情使用这些前人造的轮子。但由于大多数Agent工作流程是高度定制化的，所以团队最终仍需要自行构建许多定制化的评估，以准确捕获系统特有的问题。