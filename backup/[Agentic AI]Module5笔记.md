高度自治智能体的模式（Patterns for Highly Autonomous Agents）

### 一、Planning workflows 规划工作流

对于highly autonomous agent，会有planning的概念：即给LLM一套工具，给一个系统提示词，LLM根据问题自主规划工作流。

<img width="800" height="400" alt="Image" src="https://github.com/user-attachments/assets/81465a4c-3127-4097-9d9d-38e43a15d3c0" />

优点：无需硬编码，对于不同的问题，LLM可以自行规划工作流
缺点：可控性相对差
应用：planning在coding的应用场景已经有应用，比如让LLM编写软件构成一个复杂的应用，LLM可能会先给出一个计划；在其他应用场景，planning也有广阔的应用前景。


### 二、Planning 实现细节

1. 用JSON格式输出计划，使其对下游代码更清晰

<img width="800" height="400" alt="Image" src="https://github.com/user-attachments/assets/59c93ca4-64bb-4a90-84f7-e29c7f5944d0" />

2.  Planning with code execution，让LLM编写代码（where LLM 训练的比较好，其中的函数都见过使用方式），在代码中体现planning

<img width="750" height="430" alt="Image" src="https://github.com/user-attachments/assets/1a470d87-0e5b-4614-900a-1fcea9aa8a16" />



当能够使用coding完成任务时，让LLM编写代码实现planning往往比编写工具让LLM选择（planning with tools）更好，因为后者限制了LLM能处理的问题范围，而code execution使LLM能够处理相当多的问题，其planning的表现往往也更好。

<img width="1000" height="600" alt="Image" src="https://github.com/user-attachments/assets/5ac435c4-933d-4d18-8974-955d6197f2dc" />


### 三、Multi agent workflows

一个常见的疑惑是：比如我始终在用一个LLM model，只不过顺序写不同的prompt，为什么说是multi-agent呢？其实multi-agent workflow可以看作是一种mindset，一种分解复杂任务的方式：在你面对一个复杂任务时，instead of考虑怎样让一个人完成这个任务，考虑我需要hire什么样的团队，需要哪些特长职能的人来完成这个工作，会便于自然地将复杂任务**分解成子任务**或子进程。

<img width="650" height="400" alt="Image" src="https://github.com/user-attachments/assets/ee0bcd89-f3d2-46a3-9d11-727c63c0ab29" />


对于agents的合作，大致有两种方式：一种是线性合作，工作流是前后依赖、顺序完成、串联的；还有一种是先由一个LLM（其实相当于一个manager agent）进行分工或规划。与之前讲的规划对应，其实相当于原先用于规划的调用工具变成了调用agents。


<img width="700" height="400" alt="Image" src="https://github.com/user-attachments/assets/b662b6dd-373b-4fe1-9840-6daafaad1c04" />


<img width="750" height="400" alt="Image" src="https://github.com/user-attachments/assets/2ef5c081-7fac-4ac8-8bfe-aaeb7a592901" />


### 四、Communication patterns for multi-agent workflows

在三中提到的两个方式，其实也对应两种不同的agent间的通信或沟通方式。对于多智能体系统，communication pattern是非常重要的设计点，同时也是一个比较难的研究方向。


1、线性沟通方式（linear）

<img width="750" height="350" alt="Image" src="https://github.com/user-attachments/assets/c7c6fa5c-a692-4c80-832a-4837f376d880" />


2、层级沟通方式（hierarchical）

<img width="750" height="360" alt="Image" src="https://github.com/user-attachments/assets/d5d1d120-6058-4b42-9375-df3378b256b9" />


<img width="1558" height="851" alt="Image" src="https://github.com/user-attachments/assets/d8c27225-07c8-4a7b-9ee1-5a2ff31b4a99" />



3、其他沟通方式

<img width="511" height="381" alt="Image" src="https://github.com/user-attachments/assets/ec4ac01f-d767-442d-8a9a-0055319af4c7" />


如果系统的应用允许一定程度的混乱或不可控性（比如设计一个宣传手册，允许一次结果不好就再跑一次），可以尝试这种更难的沟通方式



___

### 本课程的总结


<img width="1523" height="876" alt="Image" src="https://github.com/user-attachments/assets/0a1cb7c7-6899-4cff-81f8-cec1958bbcfd" />




> 我觉得总的来说在这次课程中我从两个层面获得了收获：一个是building agentic workflow，学到了key design patterns including reflection,tool calls,planning,multi-agents collaboration；另一个是对于我的工作流，对于一个系统工程，如何科学地开发和指导时间投入，比如end-to-end evals，error analysis，component-level evals，以及开发的时候先做出一个quick dirty prototype，然后在build和analysis之间来回切换。其他的收获包括对LLM及其能力的更深认识

完结撒花！！！


<img width="1459" height="878" alt="Image" src="https://github.com/user-attachments/assets/362ff883-0956-463a-b60b-c814e3cb496c" />




