> 学习讲座参考：https://bit.ly/4ooS2zI


**一、What is Claude Code？—— a highly agentic coding assistant**


<img width="1150" height="500" alt="Image" src="https://github.com/user-attachments/assets/76180f75-6187-4430-803f-3b0751f91bd7" />


claude code通过一个轻量级框架（a very lightweight harness），使大模型更加智能（或者说把LLM变成一个更好的coding assistant）。


<img width="920" height="430" alt="Image" src="https://github.com/user-attachments/assets/e8a747ba-76fa-4188-bb89-b5970de54071" />




1. **Tool Use**：claude code tools见下图

<img width="500" height="458" alt="Image" src="https://github.com/user-attachments/assets/ab44d714-3894-46ce-8eea-fe8bdf03d787" />



<img width="198" height="145" alt="Image" src="https://github.com/user-attachments/assets/4c394659-2fcb-4550-a437-a8c7ec5fd90d" />



claude code使用叫做agentic search的技术，在你的代码库中寻找特定内容，而不需要让你的整个代码库离开当前的ecosystem，交给outside server做index。

<img width="1100" height="428" alt="Image" src="https://github.com/user-attachments/assets/b8a300ee-7d49-4097-8bc3-8bcb667164a0" />



2. **Memory**：

<img width="1019" height="460" alt="Image" src="https://github.com/user-attachments/assets/98ce71a5-107a-4f83-bc16-260dce65814c" />




___
___



**二、setup and codebase understanding**

claude code是一个出色的工程师，也是一个甚至更好的解释者（explainer）。使用claude code帮你快速上手codebase、dataset等，让它向你解释。


在使用claude code时，**建议第一件事是运行命令/init**（Initialize a new CLAUD.md file with codebase documentation）。CLAUD.md is mission critical，它为claude引入记忆功能，里面存储所有你想让claude在每次工作于这个codebas时，所拥有的**长期记忆**。


<img width="600" height="265" alt="Image" src="https://github.com/user-attachments/assets/e508053b-0608-4ce8-b597-db4fc979d744" />




如果在IDE（里的终端）比如VS code中使用claude code，可以用**命令/ide**获得更好的体验。

想要改变CLAUDE.md，可以直接修改，也可以**使用#来添加内容**（此时还可以选择添加到三种CLAUDE.md中的哪一种）。

e.g.

<img width="575" height="195" alt="Image" src="https://github.com/user-attachments/assets/aa098330-9413-4b02-934a-9723b7a063b9" />




**其他有用的命令：**

> /help：show help and available commands
> /clear：clear up conversation history and free up context
> /compact：clear conversation history but keep a summary in context
> esc键：中断当前进程


另：claude code对与**git**合作的良好支持，比如commit等工作可以直接提示claude code去做，而不用手写git 命令。



___
___




**三、adding features**


<img width="750" height="280" alt="Image" src="https://github.com/user-attachments/assets/dcd628b7-e205-4073-97ac-fcebca6cd008" />




**重要技巧：**

> 1. @+文档路径：向claude code指明特定文档
> 2. shift+tab  shift+tab：plan mode。做复杂工作时，我们总是建议先打开plan模式。
> 3. 图像理解能力：美化UI的时候，可以截图给claude code看（Alt+v to paste images）
> 4. 另：输入时如果想换行，可以先打slash再打回车。
> 5. add MCP：比如MCP Playwright




___
___



**三、testing, error debuging and code refactoring**


e.g. instead of直接把错误截图并简单描述给claude code，我们明确要求claude**编写test来系统化地检查问题**。



<img width="795" height="315" alt="Image" src="https://github.com/user-attachments/assets/3a33e044-8369-4eb1-b01f-ae04e8361906" />




（借助task工具）同时使用多个sub-agent工作in parallel
 
e.g.










