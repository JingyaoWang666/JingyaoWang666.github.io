### 一、控制器概述


**1.控制器的功能**
取指令——>分析指令——>执行指令（包括总线管理、中断异常处理等）
控制单元根本任务：根据指令要求依次发出一系控制信号（控制一系列受控门）


<img width="655" height="500" alt="Image" src="https://github.com/user-attachments/assets/00f77469-cb1c-4cf4-8abf-16fcefc71fda" />


**2.指令周期**
包括：取指周期、间址周期、执行周期、中断周期。

（1）取指周期：从内存中取得指令，并分析。
（2）间址周期：发出指令中的形式地址，从内存中读回有效地址。
（3）执行周期：完成指令的功能。
（4）中断周期


**3.机器周期**
指令执行的每个阶段，称为一个机器周期。

周期长度：取决于每条指令执行的步骤，每一个步骤需要的时间长度，以最慢的指令执行时间为准。

时间最长的操作——访问内存。
指令字长=存储字长的话，访存周期（取指周期）=机器周期

<img width="700" height="500" alt="Image" src="https://github.com/user-attachments/assets/6a7f9de8-6ef7-4f49-94af-de2f51b27a18" />


**4.时钟周期**
时钟周期是控制计算机操作的最小单位时间。用时钟周期控制微操作命令，每个时钟周期产生一个或几个微操作命令。（产生方式：计数器+译码器）

<img width="680" height="500" alt="Image" src="https://github.com/user-attachments/assets/6af1196f-5b30-4864-9c6a-5eca0c1acfcd" />



**5.多级时序系统**

<img width="680" height="500" alt="Image" src="https://github.com/user-attachments/assets/71f291e8-0e66-4b01-80d0-d8dc3172a25e" />










