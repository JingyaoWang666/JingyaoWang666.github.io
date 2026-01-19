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
所以，error analysis也可以看作是模块级（component level）的evals。


<img width="740" height="300" alt="Image" src="https://github.com/user-attachments/assets/c7f3e7c3-8d9c-49bc-a0ad-0dd578d7de31" />


> 其实上面谈到的评估evals、错误分析error analysis，不仅仅是agentic workflow，我们自己的工作系统也是同样适用！

