- [51单片机应用从0开始](#51------0--)
- [第一章单片机基本概念](#----------)
  * [定义](#--)
  * [单片机的功能部件](#--------)
    + [中央处理器CPU](#-----cpu)
      - [1.  运算器——中央处理器CPU](#1------------cpu)
      - [2. 控制器——中央处理器CPU](#2-----------cpu)
      - [3.  指令寄存器和指令译码器——中央处理器CPU](#3--------------------cpu)
      - [4. 程序计数器PC（Program Counter）](#4------pc-program-counter-)
      - [5. 堆栈指针SP（Stack Pointer）——中央处理器CPU](#5-----sp-stack-pointer--------cpu)
      - [6. 数据指针寄存器DPTR——中央处理器CPU](#6--------dptr-------cpu)
    + [存储器](#---)
      - [1. 程序存储器ROM](#1------rom)
      - [2. 内部数据存储器](#2--------)
      - [3. 外部数据存储器](#3--------)
    + [并行输入/输出接口](#---------)
      - [1. P0口](#1-p0-)
      - [2. P1、P2和P3口](#2-p1-p2-p3-)
    + [串行口](#---)
    + [定时器/计数器](#-------)
    + [中断控制系统](#------)
    + [时钟电路](#----)
      - [1. 机器周期和指令周期——单片机工作的基本时序](#1----------------------)
      - [2. MCS - 51 指令的取指/执行时序](#2-mcs---51-----------)
      - [3. 访问外部ROM和RAM的时序](#3-----rom-ram---)
    + [总线](#--)
    + [总结_MCS -51单片机硬件结构&MCS - 51单片机的内部结构](#---mcs--51--------mcs---51--------)
- [特点](#--)
  * [- 严格区分ROM和RAM](#------rom-ram)
  * [- 采用面向控制的指令系统](#-------------)
  * [- I/O引脚通常为多功能](#--i-o--------)
  * [- 外部扩展能力强](#---------)
  * [- 结构功能优化](#--------)
  * [- 可靠性高](#------)
- [第二章 MCS-51单片机的指令系统](#----mcs-51--------)
  * [1. 指令系统定义](#1-------)
  * [2. 单片机指令](#2------)
    + [2.1MCS-51单片机指令——分类](#21mcs-51---------)
      - [2.1.1 按指令所占的字节数](#211----------)
      - [2.1.2 按指令的执行时间](#212---------)
      - [2.1.3 按指令的功能](#213-------)
    + [2.2 MCS-51单片机指令——格式](#22-mcs-51---------)
    + [2.3 单片机指令——常用符号](#23------------)
  * [3. 寻址方式](#3-----)
    + [3.1 MCS-51单片机寻址方式——立即寻址](#31-mcs-51-------------)
    + [3.2 寻址方式——寄存器寻址](#32------------)
    + [3.3 寻址方式——寄存器间接寻址](#33--------------)
    + [3.4 寻址方式——直接寻址](#34-----------)
    + [3.5 寻址方式——变址寻址](#35-----------)
    + [3.6 寻址方式——相对寻址](#36-----------)
    + [3.7 寻址方式——位寻址](#37----------)
    + [3.8 寻址方式总结](#38-------)
  * [4. 数据传送类指令](#4--------)
    + [4.1 以累加器A为目的操作数的传送指令（4条）](#41-----a------------4--)
    + [4.2 以寄存器Rn为目的操作数的传送指令（3条）](#42-----rn------------3--)
    + [4.3 以直接地址为目的操作数的传送指令（5条） ](#43------------------5----)
    + [4.4 以间接地址为目的操作数的传送指令（3条） ](#44------------------3----)
    + [4.5 查表指令（2条） ](#45------2----)
    + [4.6 累加器A与片外数据存储器的传送指令（4条） ](#46----a--------------4----)
    + [4.7 堆栈操作指令（2条） ](#47--------2----)
    + [4.8 交换指令（5条）](#48------5--)
    + [4.9 16位数据传送指令（1条）](#49-16--------1--)
  * [5 算术运算类指令 ](#5----------)
    + [5.1 加法指令（4条）](#51------4--)
    + [5.2 带进位加法指令（4条）](#52---------4--)
    + [5.3 带借位减法指令（4条）](#53---------4--)
    + [5.4 乘法指令（1条）](#54------1--)
    + [5.5 除法指令（1条）](#55------1--)
    + [5.5 除法指令（1条）](#55------1---1)
    + [5.6 加1指令（5条）](#56--1---5--)
    + [5.7 减1指令（4条）](#57--1---4--)
    + [5.8 十进制调整指令（1条）](#58---------1--)
  * [6 逻辑操作指令](#6-------)
    + [6.1 清零指令（1条）](#61------1--)
    + [6.2 求反指令（1条）](#62------1--)
    + [6.3 循环移位指令（4条）](#63--------4--)
    + [6.4 逻辑与操作指令（6条）](#64---------6--)
    + [6.4 逻辑或操作指令（6条）](#64---------6--)
    + [6.5 逻辑异或操作指令（6条）](#65----------6--)
  * [7 控制转移类指令](#7--------)
    + [7.1无条件转移指令（4条）](#71--------4--)
    + [7.2 条件转移指令（8条）](#72--------8--)
    + [7.2 条件转移指令（8条）](#72--------8---1)
- [第5章MCS - 51单片机的中断](#-5-mcs---51------)
  * [5.1 中断的概述](#51------)
    + [5.1.1. 中断](#511---)
    + [5.1.2. 中断源](#512----)
    + [5.1.3. 中断优先级](#513------)
    + [5.1.4. 中断响应的过程](#514--------)
  * [5.2 MCS - 51中断系统](#52-mcs---51----)
  * [5.2.1 中断源](#521----)
  * [5.2.2 中断控制](#522-----)
    + [5.2.3 中断响应](#523-----)
  * [5.3 中断系统的应用](#53--------)
- [第6章 MCS - 51单片机内部定时器/ 计数器及串行接口](#-6--mcs---51------------------)
  * [6.1 定时器/计数器的结构及工作原理](#61----------------)
    + [6.1 定时器/计数器的结构及工作原理](#61-----------------1)
    + [6.2 方式和控制寄存器](#62---------)
      - [一、定时器/计数器的方式寄存器TMOD](#---------------tmod)
        * [1. M1M0工作方式控制位](#1-m1m0-------)
        * [2. C/T定时器方式或计数器方式选择位](#2-c-t--------------)
        * [3. GATE 定时器/计数器运行门控标志位](#3-gate---------------)
      - [二、定时器/计数器控制寄存器TCON](#--------------tcon)
    + [6.3 工作方式](#63-----)
      - [一、方式 0](#-----0)
      - [二、方式 1](#-----1)
      - [三、方式 2](#-----2)
      - [四、方式 3](#-----3)
  * [6.4 定时器/计数器应用举例](#64------------)
    + [一、方式 0 的应用例 1 利用定时器输出周期为 2 ms的方波, 设单片机晶振频率为 6 MHz。](#-----0------1------------2-ms---------------6-mhz-)
  * [6.5 MCS - 51单片机的串行接口](#65-mcs---51--------)
  * [6.6 串行口的应用](#66-------)
  * [5. 算数运算类指令](#5--------)
  * [6. 逻辑操作类指令](#6--------)
  * [7. 控制转移类指令](#7--------)
  * [8. 位操作类指令](#8-------)
- [第三章 第一个单片机系统](#------------)

没写完。
@[toc](目录)
# 51单片机应用从0开始
# 第一章单片机基本概念
## 定义
 把中央处理器CPU（Central Processing Unit）、存储器（Memory）、定时器/计数器、中断、输入/输出I/O（Input/Output）接口电路等功能部件集成在一块集成电路芯片上的微型计算机。
 ![基本概念](https://img-blog.csdnimg.cn/2020041521150083.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
## 单片机的功能部件
### 中央处理器CPU
计算机的核心部件 由运算器和控制器组成 主要完成计算机的运算和控制功能

#### 1.  运算器——中央处理器CPU
 	- 算术逻辑单元ALU 
 	- 累加器ACC（Accumulator） 
 	- 寄存器B 
 	- 程序状态字PSW（Programe State Word）


**PSW👇** ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200416114853953.png)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200416114904433.png)
**RS1、 RS0与片内工作寄存器组的对应关系👇**
 ![RS1、 RS0与片内工作寄存器组的对应关系](https://img-blog.csdnimg.cn/20200416115709240.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
#### 2. 控制器——中央处理器CPU
 - 时钟电路
	- （a）内部时钟电路
	- （b）外部振荡源
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200416120028514.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
 - 复位电路
	- （a）上电复位电路
	- （b）开关复位电路 
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200416120124197.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
	- 复位后内部寄存器状态
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200416120409885.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
#### 3.  指令寄存器和指令译码器——中央处理器CPU 
指令寄存器中存放指令代码。CPU执行指令时, 由程序存储器中读取的指令代码送入指令存储器, 经译码器译码后由定时与控制电路发出相应的控制信号, 完成指令所指定的操作。
#### 4. 程序计数器PC（Program Counter） 
**PC用于存放CPU下一条要执行的指令地址, 是一个 16 位的专用寄存器, 可寻址范围是0000H~0FFFFH共 64 KB。 程序中的每条指令存放在==ROM区==的某一单元, 并都有自己的存放地址。** CPU 要执行哪条指令时, 就把该条指令所在 的单元的地址送上地址总线。 在顺序执行程序中, 当PC的 内容被送到地址总线后, 会自动加 1, 即(PC)← (PC)+1, 又指向CPU下一条要执行的指令地址。
#### 5. 堆栈指针SP（Stack Pointer）——中央处理器CPU 
堆栈操作是在==内存RAM区==专门开辟出来的按照“先进后出”原则进行数据存取的一种工作方式, 主要用于子程序调用及返回和中断处理断点的保护及返回, 它在完成子程序嵌套和多重中断处理中是必不可少的。为保证逐级正确返回, 进入栈区的“断点”数据应遵循“先进后出”的原则。SP用 来指示堆栈所处的位置, 在进行操作之前, 先用指令给SP赋值, 以规定栈区在RAM区的起始地址（栈底层）。当数据推入栈 区后, SP的值也自动随之变化。**MCS - 51 系统复位后, ==SP初始化为07H==。**
#### 6. 数据指针寄存器DPTR——中央处理器CPU 
**数据指针DPTR是一个 16 位的专用寄存器, 其高位字节寄存器用DPH表示,低位字节寄存器用DPL表示。既可作为一个 16 位寄存器DPTR来处理, 也可作为两个独立的 8 位寄存器DPH和DPL来处理。** 
**DPTR 主要用来存放 16 位地址, 当对 64 KB外部数据存储器空间寻址时, 作为间址寄存器用。在访问程序存储器时, 用作基址寄存器。**
### 存储器
具有记忆功能的电子部件，分为程序存储器和数据存储器两类
**程序存储器：存储程序、表格等相对固定的信息 
数据存储器：存储程序运行期间所用到的数据信息**
 #### 1. 程序存储器ROM
 - **对于8051来说, 程序存储器（ROM）的内部地址为0000H~0FFFH, 共 4 KB; 外部地址为 1000H~FFFFH, 共 60 KB。** 当程序计数器由内部 0FFFH执行到外部 1000H 时, 会自动跳转。 对于 8751 来说, 内部有 4 KB的EPROM, 将它作为内部程序存 储器; 8031 内部无程序存储器, 必须外接程序存储器。 8031 最多可外扩 64 KB程序存储器, 其中 6 个单元地址具有特殊用途, 是保留给系统使用的。**0000H是系统的启动地址, 一般在该单元中存放一条绝对跳转指令。0003H、000BH、 000BH、001BH和 0023H对应 5 种中断源的中断服务入口地址。**
 #### 2. 内部数据存储器 
- MCS-51 单片机片内RAM的配置如下图所示。**片内RAM为 256 字节, 地址范围为00H~FFH, 分为两大部分: 低 128 字节（00H~7FH）为真正的RAM区; 高 128 字节 （80H~FFH）为特殊功能寄存器区SFR。 在低 128 字节RAM中, 00H~1FH共 32 单元是 4 个通用**
**工作寄存器区。每一个区有 8 个通用寄存器R0~R7。寄存器和RAM地址对应关系如表 。**
寄存器与RAM 地址对照表👇![在这里插入图片描述](https://img-blog.csdnimg.cn/2020041718090977.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
RAM中的位寻址区地址表👇
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020041718101265.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
SFR特殊功能寄存器地址表1👇
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200417181038492.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
SFR特殊功能寄存器地址表2👇
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020041718111885.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
SFR特殊功能寄存器地址表3👇![在这里插入图片描述](https://img-blog.csdnimg.cn/20200417181133173.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
#### 3. 外部数据存储器 
外部数据存储器一般由静态RAM构成，其容量大小由用户根据需要而定, 最大可扩展到 64 KB RAM , 地址是 0000H~0FFFFH。 **CPU通过MOVX指令访问外部数据存储器, 用间接寻址方式, R0、R1和 DPTR都可作间接寄存器**。注意, 外部RAM和扩展的I/O接口是统一编址的, 所有的外扩I/O 口都要占用 64 KB中的地址单元。

### 并行输入/输出接口
CPU与相应的I/O设备（如: 键盘、鼠标、显示器、打印机等）进行信息交换的桥梁, 
主要功能是协调、匹配CPU与外设的工作
#### 1. P0口

P0 口内部一位结构图👇![在这里插入图片描述](https://img-blog.csdnimg.cn/2020041718222917.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
#### 2. P1、P2和P3口 
P1、P2 和P3 口为准双向口, 在内部差别不大, 但使用功能有所不同。 
P1口是用户专用 8 位准双向I/O口, 具有通用输入/输出功能, 每一位都能独立地设定为输入或输出。当有输出方式变为输入 方式时, 该位的锁存器必须写入“1”, 然后才能进入输入操作。 
P2口是 8 位准双向I/O口。外接I/O设备时, 可作为扩展系统的地址总线, 输出高8位地址, 与P0 口一起组成 16 位地址总线。 对于 8031 而言, P2 口一般只作为地址总线使用, 而不作为I/O线 直接与外部设备相连。
P3口的第二功能👇
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200417182616341.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
单片机的引脚及其功能👇
- (a) 管脚图；
- (b) 8031 引脚功能分类
- ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200417182706294.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)

### 串行口
实现单片机和其他设备之间的串行数据传送 
即可作为全双工异步通用收发器使用，又可作为同步移位寄存器使用。
### 定时器/计数器
用于实现定时或计数功能
并以其定时或计数结果对操作对象进行控制
### 中断控制系统
为满足各种实时控制的需要而设置 
是重要的输入输出方式 
8051单片机中有5个中断源，可分为高级和低级两个优先级别。
### 时钟电路
__主要由振荡器和分频器组成__
为系统各工作部件提供时间基准 
串口、中断、定时/计数是单片机重要的内部资源 
为CPU控制外部设备、实现信息交流提供了强有力的支持
#### 1. 机器周期和指令周期——单片机工作的基本时序
-（1）振荡周期: 也称时钟周期, 是指为单片机提供时钟脉冲信号的振荡源的周期。
-（2）状态周期: 每个状态周期为时钟周期的 2 倍, 是振荡周期经二分频后得到的。
-（3）机器周期: 一个机器周期包含 6 个状态周期S1~S6, 也就是 12 个时钟周期。 在一个机器周期内, CPU可以完成一个独立的操作。
-（4） 指令周期: 它是指CPU完成一条操作所需的全部时间。 每条指令执行时间都是有一个或几个机器周期组成。MCS 51 系统中, 有单周期指令、双周期指令和四周期指令。
#### 2. MCS - 51 指令的取指/执行时序
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020041718481331.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
#### 3. 访问外部ROM和RAM的时序

读外部程序ROM时序👇
![在这里插入图片描述](https://img-blog.csdnimg.cn/202004171848454.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
读外部数据RAM时序 👇
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200417184930738.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
写外部数据RAM的时序👇
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200417185021663.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
### 总线
计算机各工作部件之间传送信息的公共通道 
按功能可分为

 - 数据总线DB（Data Bus）
 - 地址总线 AB（Address Bus）
 - 控制总线 CB（Control Bus）
三类分别传送数据信息、地址信息和控制信息
### 总结_MCS -51单片机硬件结构&MCS - 51单片机的内部结构
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200417184239714.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)




# 特点

## - 严格区分ROM和RAM
	 - 程序存储器（ROM）只存放程序、固定常数及数据表格
	 - 数据存储器（RAM）用作工作区及存放用户数据
	 - 小容量的数据存储器能以高速RAM形式集成在单片机内，以 加速单片机的执行速度
## - 采用面向控制的指令系统
 	- 为满足控制的需要，单片机有强大的逻辑控制能力，特别是 具有很强的位处理能力。
## - I/O引脚通常为多功能
 	- 引脚处于何种功能，可由指令来设置或由机器状态来区分 
 	- 解决实际引脚数和需要的信号线的矛盾
## - 外部扩展能力强
	- 在内部的各种功能部件不能满足应用需要时，均可在外部进 行扩展
	- （如扩展ROM、RAM，I/O接口，定时器/计数器， 中断系统等）
	- 与许多通用的微机接口芯片兼容 
	- 给应用系统设计带来极大的方便和灵活性。
## - 结构功能优化
	- 能方便灵活地组成各种智能测控仪器仪表和设备
## - 可靠性高
	- 单片机芯片按工业测校环境要求设计 
	- 产品在120°C温度条件下经44小时老化处理，并通 过电气测试及最终质量检验
	- 可以适应各种恶劣的工作环境。
 
 

---
--- 
# 第二章 MCS-51单片机的指令系统
## 1. 指令系统定义
- 指令是规定计算机完成一个特定功能的命令 • MCS-51单片机设有传送、算术运算、逻辑运算、控制转移、位操作共5 类111条指令
- 用户可以通过==立即寻址、寄存器寻址、寄存器间接寻址、直接寻址、变址 寻址、相对寻址、位寻址==等7种寻址方式规定操作数
- 深入理解不同寻址方式的特点及功能，全面掌握各条指令的格式、功能及 使用方法是灵活运用指令系统的关键。
## 2. 单片机指令
### 2.1MCS-51单片机指令——分类
#### 2.1.1 按指令所占的字节数
- 单字节指令（49条） 
- 双字节指令（46条） 
- 三字节指令（16条）
#### 2.1.2 按指令的执行时间
- 单周期指令（65条） 
- 双周期指令（44条） 
- 四周期指令（2条）
#### 2.1.3 按指令的功能
- 数据传送类指令（29条） 
- 算术运算类指令（24条） 
- 逻辑运算类指令（24条） 
- 控制转移类指令（17条）
- 位操作类指令（17条）
### 2.2 MCS-51单片机指令——格式
==[标号: ] 操作码助记符 [目的操作数][, 源操作数] [;注释]==
【例】AA: ADD A, #10H ;将累加器A的内容与10H相加，结果存入累加器A 
- AA为标号，是这条指令的标志，其值是该条指令的首地址 
- ADD为操作码，说明要进行加法运算 
- 目的操作数为累加器A，源操作数为#10H 
- “;”后面为注释部分
### 2.3 单片机指令——常用符号
为清晰准确地表述指令的格式及功能，下面对MCS-51单片机指令中常用的符号作一些规定：
 1. A（ACC）：累加器
 2. B：专用寄存器，用于乘法和除法指令中 
 3. C：进位标志或进位位，或布尔处理机中的累加位(器) 
 4. DPTR：数据指针，可用作16位地址寄存器 
 5. Rn（n=0~7）：当前寄存器组的8个工作寄存器R0~R7，由PSW中的 RS1、RS0决定当前使用的寄存器组。
 6. Ri（i=0或1）：可用于间接寻址的两个寄存器R0、R1
 7. #data：8位立即数，即出现在指令中直接参与操作的操作数 
 8.  #data16：16位立即数 
 9. rel：以补码形式表示的8位相对偏移量，范围为-128~127，主要用在相对寻址的指令中
 10. addr16和addr11：分别表示16位直接地址和11位直接地址，即存放操作数的存储器地址。
 11. direct：表示内部数据存贮器单元的地址或特殊功能寄存器SFR的地址， 对SFR而言，既可使用它的物理地址，也可直接使用它的名字。
 12. ＠：间接寻址中工作寄存器的前缀符号
 13. ==(X) ：X单元中的内容== 
 14. bit ：表示内部RAM和SFR中的某些具有位寻址功能的位地址。SFR中的 位地址可以直接出现在指令中，为了阅读方便，往往也可用SFR的名字和 所在的数位表示。如：表示PSW中的奇偶校验位，可写成D0H，也可写 成PSW.0的形式。
 15. ==((X)) ：以X单元的内容为地址的存储器单元内容，即(X)作地址，该地址 单元的内容用((X))表示。==
 16. ==$：当前指令的地址== 
 17. ==/ ：对该位操作数取反，但不影响该位的原值== 
 18. →：表示操作流程，将箭尾一方的内容送入箭头所指的另一方单元中

## 3. 寻址方式
### 3.1 MCS-51单片机寻址方式——立即寻址

 - 定义：指操作数包括在指令字节中，紧跟在操作码的后面，作为指令的一 部分与操作码一起存放在程序存储器中，可以立即得到并执行，不需要经 过别的途径去寻找，故称为立即寻址。
 - 汇编指令中，在一个数的前面冠以"#"符号作为前缀，就表示该操作数为立即数。
 - 【例】==MOV A, #52H ;A←52H ==
	 - MOV DPTR, #5678H ;DPTR←5678H
 - ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200422183455326.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
### 3.2 寻址方式——寄存器寻址
 
 - 定义：指令指定寄存器的名字，寄存器的内容为操作数 
 	- ==【例】MOV A, R0		;A← (R0)==
	- 该指令的功能是把源寄存器R0中的内容传送到累加器A中，如R0中的 内容为30H，则执行该指令后A的内容也为30H。
	 - 可用于寄存器寻址的寄存器有： • 四组工作寄存器R0~R7共32个，但每次只能使用当前寄存器组中的8 个。
	 - 部分特殊功能寄存器A、B、DPTR等。

### 3.3 寻址方式——寄存器间接寻址

 - 规定如下： 
	 - 片内基本RAM的低128B、高128B，间接用Ri，即@R1, @R0 
	 - 片外RAM（64KB）：间接用DPTR，即@DPTR 
	 - 片外扩展RAM：若小于256B，可用@DPTR或@R1, @R0，若大于256字 节，间接用DPTR，即@DPTR
	 - **注意：寄存器间接寻址方式不能用于对特殊功能寄存器SFR的寻址** 
	 -  【例】==MOV DPTR, #3456H 	;DPTR ←3456H
	 	       MOVX A, @DPTR		;A ←((DPTR))==
	 - 是把DPTR寄存器的作为地址单元，从这个地址单元中取出内容传送给A， 假设（3456H)=99H，指令运行后（A)=99H。

### 3.4 寻址方式——直接寻址
- 指令中直接给出操作数的存储器地址，操作数在存储器中。 
- 【例】==MOV A, 52H	;A←(52H)==
- ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200428184056989.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
指令中52H为操作数的存储器地址
该指令的功能是把片内RAM地址为52H单元的内容送到A中,A的地址是E0H
该指令的机器码为E5H 52H。
### 3.5 寻址方式——变址寻址 

变址寻址指令具有以下三个特点：
1. 指令操作码内隐含有作为基地址寄存器用的数据指针DPTR或程序计数器PC，其中DPTR或PC中应预先存放有操作数的相应基地址。
2. 指令操作码内也含有累加器A，累加器A中应预先存放有被寻址操作数地址对基地址的偏移量，该地址偏移量应是一个00H～0FFH范围内的无符号数。
3. 在执行变址寻址指令时，单片机先把基地址和地址偏移量相加，以形成操作数的有效地址。
- MCS-51单片机共有三条变址指令 
- MOVC A, @A+PC		;A←((A)+(PC))
- MOVC A, @A+DPTR 	;A←((A)+(DPTR))
- JMP @A+DPTR		;PC←(A)+(DPTR)
- 前两条指令是在程序存储器中取操作数 
- 第三条指令是要获得程序的跳转地址，实现程序的转移。

- 【例】MOV A, #22H 
- MOV DPTR, #63A0H 
- MOV A, @A+DPTR	;A←((A)+(DPTR))
- ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429145514148.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
### 3.6 寻址方式——相对寻址 
- 相对寻址以程序计数器PC的当前值作为基地址，与指令中给出的相对偏移量rel进行相加，把所得之和作为程序的转移地址。
- 使用时注意以下两点 
1. ==当前PC值是指相对转移指令的存储地址加上该指令的字节数 ==
【例】JZ rel 是一条累加器A为零就转移的双字节指令。**若该指令的存储地址为2050H，则执行该指令时的当前PC值即为2052H。**即当前PC值是相对转移指令取指结束时的值。 
2. 偏移量rel是有符号的单字节数，以补码表示，其取值范围是-128~+127 （00H~FFH）。**负数表示从当前地址向地址小的方向转移，正数表示从当前地址向地址大的方向转移。**所以，相对转移指令满足条件后，转移的目标地址为:
==目标地址 ＝ 当前PC值 + rel ＝ 指令存储地址 + 指令字节数 + rel==
【例】SJMP 08H	;PC←PC+2+08H
• 这是一条转移指令，设PC当前值＝2000H，PC＋2＝2002H因此程序转向(PC)+2+rel＝2000H＋2＋08H ＝200AH单元。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429151743198.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)

### 3.7 寻址方式——位寻址
 为了使程序设计方便，MCS-51指令系统提供了多种位地址的表示方式，可归纳为4种形式： 
1. 直接使用位地址 
【例】MOV C, 0D5H	;将PSW的位5（位地址D5H）的状态送进位标志位。
2. 单元地址加位序号的形式 
【例】MOV C, 0D0H.5	;将PSW（单元地址0D0H）的位5（位地址D5H）的状态送进位标志位。
3. 特殊功能寄存器符号加位序号的形式 
【例】MOV C, PSW.5	;将PSW的位5的状态送进位标志位。
4. 位名称表示形式 
【例】MOV C, F0	;将PSW的位5（位地址D5H、位名称为F0）的状态送进位标志位。

### 3.8 寻址方式总结 
- 寻址方式与寻址空间的关系
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429153129951.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
- 寻址方式与存储空间的关系
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020042915332037.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)

## 4. 数据传送类指令
- 数据传送类指令用到的助记符有：**MOV，MOVX，MOVC，XCH， XCHD，PUSH，POP，SWAP**。
- 一般格式：**MOV [目的操作数], [源操作数]** 
- 一般功能：**目的操作数 ← 源操作数中的数据** 
- 源操作数可以是：A、Rn、direct、@Ri、#data 
- 目的操作数可以是：A、Rn、direct、@Ri 
- 数据传送指令一般不影响标志，只有一种堆栈操作可能直接修改程序状态 字PSW。
- 如果目的操作数为ACC，将会影响奇偶标志P。
### 4.1 以累加器A为目的操作数的传送指令（4条）
- 功能：把源操作数送到累加器A 
- 有直接、立即数、寄存器和寄存器间接寻址方式
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429154336178.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
【例】 设外部RAM（2023H)=0FH，执行以下程序段： 
MOV DPTR, #2023H 	;DPTR←2023H 
MOVX A, @DPTR		;A←((DPTR)) 
MOV 30H, A 			;30H←(A)
MOV A, #00H			;A←00H
**MOVX @DPTR, A		;((DPTR))←(A)DPTR所指向的内容赋予00H**
程序段执行后，(DPTR)=2023H，(30H)=0FH， (A)=00H，**(2023H)=00H**，表示把片外RAM 2023H单元的内容0FH送到内部RAM的30H单 元，然后把外部RAM 2023H单元和累加器A清0。
### 4.2 以寄存器Rn为目的操作数的传送指令（3条） 
- 功能：把源操作数送到所选定的工作寄存器Rn中 
- 有直接、立即数和寄存器寻址方式 
- 注意：没有 
- **MOV Rn, Rn；**
- **MOV Rn, @Ri；**
- **MOV @Ri, Rn**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429154932691.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
【例】设内部RAM(30H)=40H，(40H)=10H，(10H)=00H，(P1)=0CAH，分析以下程序执行后，各单元、寄存器、P2口的内容。 
MOV R0, #30H	;R0←30H
MOV A, @R0 		;A←((R0))
MOV R1, A		;R1←(A) 
MOV B, @R1 		;B←((R1))
MOV @R1, P1 	;((R1))←(P1)
MOV P2, P1		;P2←(P1)
MOV 10H, #20H	;10H←20H
执行上述指令后，(R0)=30H；(R1)=(A)=40H；(B)=10H； (40H)=(P1)=(P2)=0CAH；(10H)=20H。
###	4.3 以直接地址为目的操作数的传送指令（5条）  
- 功能：把源操作数送到由直接地址direct所选定的片内RAM中  
- 有直接、立即、寄存器和寄存器间接4种寻址方式  
- 注意：==MOV direct1, direct2，翻译成机器码时，源地址在前，目的地址在后。==；一般格式：**MOV [目的操作数], [源操作数]**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429164031272.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
### 4.4 以间接地址为目的操作数的传送指令（3条）  
- 功能：把源操作数送到以Ri中的内容为地址的片内RAM中  
- 有直接、立即和寄存器3种寻址方式
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429164146628.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
### 4.5 查表指令（2条）  
- 功能：对存放于程序存储器中的数据表格进行查找传送  
- 使用变址寻址方式
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429164417715.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
【例】编一查表程序，将内部RAM40H单元内的数（0~9）的平方存入内 部RAM50H单元。先作一个0~9的平方表，存入TAB中。然后用查表指令 实现上述功能。 
MOV A, 40H			;40H单元的数送A 
MOV DPTR, #TAB		;DP
MOVC A, @A+DPTR 	;查表 
MOV 50H, A 			;查表得到的平方值，存50HTR指向表头
SJMP $ 				;等待
TAB: 0, 1, 4, 9, ……81
### 4.6 累加器A与片外数据存储器的传送指令（4条）  
- 这4条指令的功能是实现累加器A与片外RAM间的数据传送。使用寄存器寻址方式
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429175418445.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
### 4.7 堆栈操作指令（2条）  
- 堆栈操作有进栈和出栈，即可以压入和弹出数据，常用于保存或恢复现场。  
- 进栈指令：保存片内RAM单元(低128字节)或特殊功能寄存器SFR的内容  
- 出栈指令：恢复片内RAM单元(低128字节)或特殊功能寄存器SFR的内容
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429175838368.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
- 单片机开机复位后，(SP)默认为07H，但一般都需要重新赋值，设置新的 SP首址。
- 入栈的第一个数据必须存放于SP+1所指存储单元，故实际的堆栈底为SP 初值+1所指的存储单元。
- 注意：对于累加器来说，在堆栈指令中只能用ACC，不能用A，属于直接寻址。
【例】进入中断服务程序时，常把程序状态寄存器PSW、累加器A、数据指针DPTR进栈保护。
设当前SP为60H。则程序段 
MOV SP, #60H 
PUSH PSW 
PUSH ACC 
PUSH DPL 
PUSH DPH
执行后，SP内容修改为64H，而61H、 62H、63H、64H单元中依次存入 PSW、A、DPL、DPH的内容。
在中断服务程序结束之前，用下列程序 段恢复数据。 
POP DPH 
POP DPL 
POP ACC 
POP PSW
指令执行之后，SP内容修改为60H， 而64H、63H、62、61H单元的内容依次弹出到DPH、DPL、A、PSW中。 
保护数据时，进栈、出栈的次序一定要符合“先进后出”的原则。
### 4.8 交换指令（5条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429180649731.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429180717648.png)
- 这条指令的功能是把16位常数送入数据指针寄存器。这也是唯一一条16 位数据传送指令。 
- 【例】设(R0)＝30H，(A)＝65H，(30H)＝8FH，执行指令： 
- XCH A, @R0 	;(R0)＝30H,(A)＝8FH,(30H)＝65H
- XCHD A, @R0 	;(R0)＝30H,(A)＝6FH,(30H)＝85H
- SWAP A 		;(A)＝56H
### 4.9 16位数据传送指令（1条）
【例】将片内RAM30H单元与40H单元中的内容互换。
- 方法1（直接地址传送法） 
- MOV 31H, 30H 
- MOV 30H, 40H 
- MOV 40H, 31H 
- SJMP $
---
- 方法2（间接地址传送法） 
- MOV R0, #40H 
- MOV R1, #30H 
- MOV A, @R0 
- MOV B , @R1 
- MOV @R1, A 
- MOV @R0, B 
- SJMP $
- ---
- 方法3（字节交换传送法） 
- MOV A, 30H 
- XCH A, 40H 
- MOV 30H, A 
- SJMP $
---
- 方法4（堆栈传送法） 
- PUSH 30H 
- PUSH 40H 
- POP 30H 
- POP 40H 
- SJMP $
---
## 5 算术运算类指令  
- 算术运算指令共有24条  
- 算术运算主要是执行加、减、乘、除法四则运算  
- MCS-51指令系统中还有加1、减1操作及BCD码的运算调整  
- 虽然MCS-51单片机的算术逻辑单元ALU仅能对8位无符号整数进行运算， 但利用进位标志C，则可进行多字节无符号整数的运算。同时利用溢出标志，还可以对带符号数进行补码运算。
- 需要指出的是，除加1、减1指令外，这类指令一般都会对PSW有影响
### 5.1 加法指令（4条）
这4条指令的功能是把立即数，直接地址、工作寄存器及间接地址内容与累加器A中的内容相加，运算结果存在A中。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429183136557.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
- 各标志位的形成方法  
- 如果位7有进位输出，则置位进位标志CY，否则清CY；  
- 如果位3有进位输出，则置位半进位标志AC，否则清AC；  
- 如果位6有进位输出而位7没有，或者位7有进位输出而位6没有，则置位溢出标志OV，否则清OV，即OV=CY7⊕CY6。  
- **若累加器A中1的个数为奇数，则P=1，否则，P＝0。**
- 对于加法，溢出只能发生在两个加数符号相同的情况。在进行带符号数的加法运算时，溢出标志OV＝1表示有溢出发生（即和大于＋127或小于 ~128）。
- 【例】设(A)=85H，(R1)=30H，(30H)=0AFH，执行指令：
- ADD A,@R1
- 	1000 0101
＋ 	1010 1111 
     1 0011 0100
     执行结果为：(A)=34H, CY=1, AC=1, OV=1, P=1
### 5.2 带进位加法指令（4条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506180659350.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)

### 5.3 带借位减法指令（4条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506181511873.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
- 在进行减法运算中，CY=1表示有借位，CY=0则无借位。 
- OV=1表明带符号数相减时，从一个正数减去一个负数结果为负数，或者 从一个负数中减去一个正数结果为正数的错误情况。
- 在进行减法运算前，如果不知道借位标志位C的状态，则应先对CY进行清零操作。
- 如果要进行不带借位减法，只需把CY先清零。
- 【例】设(A)=0C9H, (R3)=54H, (CY)=1, 执行指令：SUBB A, R3
  1100 1001
 -0000 0001 

  1100 1000
- 0101 0100
  0111 0100
结果：(A)=74H, Cy=0, AC=0, OV=1, P=0
### 5.4 乘法指令（1条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506183035377.png)
在乘法运算时，如果OV=1，说明乘积大于FFH，否则OV=0，但进位标志位CY总是等于0。 
【例】若(A)=80H=128, (B)=32H=50，执行指令： MUL AB
结果：(B)=19H, (A)=00H, OV=1, CY=0
### 5.5 除法指令（1条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020050618333570.png)
- 除法运算总是使进位标志位CY等于0 
- 如果OV=1，表明寄存器B中的内容为00H，那么执行结果为不确定值， 表示除法有溢出。
- 【例】设(A)=0BFH，(B)=32H，执行指令： DIV AB
结果： (A)=03H, (B)=29H, CY=0, OV=0
### 5.5 除法指令（1条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506183832345.png)
- 除法运算总是使进位标志位CY等于0 
- 如果OV=1，表明寄存器B中的内容为00H，那么执行结果为不确定值， 表示除法有溢出。 
- 【例】设(A)=0BFH，(B)=32H，
- 执行指令： DIV AB
- 结果： (A)=03H, (B)=29H, CY=0, OV=0
### 5.6 加1指令（5条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506184053696.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
- 在INC direct指令中，如果直接地址是I/O口，其功能是先读入I/O锁存器的内容，然后在CPU进行加1操作，再输出到I/O口中，这就是“读— 修改—写”操作。
- 加1指令不影响标志。如果原寄存器的内容为FFH，执行加1后，结果就会 是00H。但不会影响标志。
### 5.7 减1指令（4条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506184240600.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
减1操作也不影响标志。若原寄存器的内容为00H，减1后为FFH，运算结 果不影响任何标志位。当直接地址是I/O口时，实现“读—修改—写” 操作。
### 5.8 十进制调整指令（1条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506184407318.png)
- 在进行BCD码运算时，这条指令总是跟在ADD或ADDC指令之后，其功能是对执行加法运算后存于累加器A中的结果进行调整。
- 注意：只能用于加法运算
- 【例】有两个BCD数36与45相加，结果应为BCD码81，程序如下： 
- MOV A, #36H 
- ADD A, #45H 
- DA A
加法指令执行后得结果7BH；
**第三条指令对累加器A中的结构进行十进制调整，低4位（为0BH）大于9，因此要加6**，最后得到调整的BCD码为81。
## 6 逻辑操作指令
### 6.1 清零指令（1条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506185108665.png)
### 6.2 求反指令（1条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506185132405.png)
### 6.3 循环移位指令（4条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506185221458.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
【例】 
MOV A, #04H ;(A)=04
RL A  ; (A)=08
RR A ;(A)=04
• 逻辑左移一位相当于乘2，逻辑右移一位相当于除2。
###  6.4 逻辑与操作指令（6条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506185522642.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
### 6.4 逻辑或操作指令（6条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506185602775.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
### 6.5 逻辑异或操作指令（6条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506185836769.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
【例】利用逻辑运算指令，可以模拟各种硬件逻辑电路。
如下图所示的组合逻辑电路，试编写一程序模拟其功能。设输入信号放在X、Y、Z单元中， 输出信号放在F单元。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506233200542.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
• 参考程序如下： 
MOV A, X 	;A ← (X)
ANL A, Y		;A ← (A) ∧ (Y)
MOV R1, A 	;A内容暂存 
MOV A, Y 	;A ← (Y)
XRL A, Z 		;A ← (Y) ⊕ (Z) 
CPL A		;A ← (Y) ⊕ (Z)
ORL A, R1	;得到输出 
MOV F, A 		;存输出
SJMP $
## 7 控制转移类指令
### 7.1无条件转移指令（4条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506233837485.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
### 7.2 条件转移指令（8条）
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020050623392398.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200506234105427.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
【例】将外部数据RAM中的一个数据块传送到内部数据RAM中，两者的首地址分别为 DATA1和TATA2，遇到传送的数据为0时停止。 
解：外部RAM向内部RAM的数据传送一定要借助于累加器A，利用累加器判零转移指令正好可以判别是否要继续传送或者终止。 
MOV DPTR, #DATA1
MOV R1, #DATA2
LOOP: MOVX A, @DPTR HERE: JZ HERE
MOV @R1, A INC DPTR
INC R1 SJMP LOOP
;外部数据块首地址 ;内部数据块首地址 ;外部数据送给A ;为0则终止
;不为0传送内部RAM数据 ;修改地址指针 ;继续循环
### 7.2 条件转移指令（8条）
【例】将外部数据RAM中的一个数据块传送到内部数据RAM中，两者的首地址分别为 DATA1和TATA2，遇到传送的数据为0时停止。
# 第5章MCS - 51单片机的中断
## 5.1 中断的概述
### 5.1.1. 中断 
中断是指计算机在执行某一程序的过程中, 由于计算机系统内、外的某种原因, 而必须中止原程序的执行, 转去执行相应的处理程序, 待处理结束之后, 再回来继续执行被中止的原程序的过程。采用了中断技术后的计算机, 可以解决CPU与外设之间速度匹配的问题, 使计算机可以及时处理系统中许多随机的参数和信息, 同时, 它也提高了计算机处理故障与应变的能力。 
### 5.1.2. 中断源 
中断源是指在计算机系统中向CPU发出中断请求的来源, 中断可以人为设定, 也可以是为响应突发性随机事件而 设置。通常有I/O设备、实时控制系统中的随机参数和信息 故障源等。
### 5.1.3. 中断优先级 
中断优先级越高, 则响应优先权就越高。当CPU正在执行中断服务程序时, 又有中断优先级更高的中断申请产生, 这时CPU就会暂停当前的中断服务转而处理高级中断申请, 待高级中断处理程序完毕再返回原中断程序断点处继续执行, 这一过程称为中断嵌套。
### 5.1.4. 中断响应的过程
(1) 在每条指令结束后, 系统都自动检测中断请求信号, 如果有中断请求，且CPU处于开中断状态下, 则响应中断。
(2) 保护现场, 在保护现场前, 一般要关中断, 以防止现场被破坏。保护现场一般是用堆栈指令将原程序中用到的寄存器推入堆栈。
(3) 中断服务, 即为相应的中断源服务。
(4) 恢复现场, 用堆栈指令将保护在堆栈中的数据弹出来, 在 恢复现场前要关中断, 以防止现场被破坏。在恢复现场后应及时开中断。
(5) 返回, 此时 CPU将推入到堆栈的断点地址弹回到程序计数器, 从而使CPU继续执行刚才被中断的程序。
## 5.2 MCS - 51中断系统
图 MCS - 51中断系统结构框图👇
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507153250749.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
在INT0或INT1口输入一个信号(低电平或下降沿)，就可以使单片机临时停下正在执行的程序，转去执行预先编内好、另外的程序。
INT0：外部中断0触发方式控制位，1表示边沿触发，0表示电平触发；
EX0：外部中断0允许位，1表示允许外部中断0的中断申请；
ET0：定时/计数器0中断允许位，1表示允许定时/计数器0的溢出中断；
IE0：外部中断0中断申请标志位，1表示有中断申请。
IT0设置触发中断的方法：单片机中IT0=1——下降沿触发（边缘触发方法），IT0=0——低电平触发（电平触发方法）
EA是总中断，开启总中断时只要用SETB EA将EA置1就行了。
Px0=1高优先级中断；px0=0低优先级中断
## 5.2.1 中断源
表  8051 中断源
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507153403752.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
1. 特殊功能寄存器TCON中的标志👇![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507153624928.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)

2. 特殊功能寄存器SCON
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507153653938.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
## 5.2.2 中断控制 
1. 中断允许控制 MCS - 51单片机有 5个（8052有 6个）中断源, 为了使每个中断源都能独立地被允许或禁止, 以便用户能灵活使用, 它在每个中断信号的通道中设置了一个中断屏蔽触发器。 只有该触发器无效, 它所对应的中断请求信号才能进入CPU, 即此类型中断开放。 否则, 即使其对应的中断标志位置 1, CPU也不会响应中断, 即此类型中断被屏蔽了。同时CPU内还设置了一个中断允许触发器, 它控制CPU能否响应中断。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507164027894.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
2. 中断优先级
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507164100733.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
表 5.2 同级内第二优先级次序👇
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507164136487.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
例如, 某软件中对寄存器IE、 IP设置如下: 
MOV IE, ＃ 8FH 
MOV IP, ＃ 06H 
则此时该系统中: 
- CPU中断允许; 
-  允许外部中断 0、外部中断 1、定时器 /计数器 0、
- 定时器 /计数器1提出的中断申请; 
- 允许中断源的中断优先次序为: 定时器 /计数器 0>外部中断 1>外部中断 0>定时器/计数器 1。
### 5.2.3 中断响应 
1. 中断响应的条件
(1）同级或高优先级的中断已在进行中; 
(2）当前的机器周期还不是正在执行指令的最后一个机器周期（换言之, 正在执行的指令完成前, 任何中断请求都得不到响应）; 
(3）正在执行的是一条 RETI或者访问特殊功能寄存器IE或 IP的指令（换言之, 在 RETI或读写 IE或 IP之后, 不会马上响应中断请求, 而至少执行一条其它指令之后才会响应）。
2.中断响应请求
单片机一旦响应中断请求, 就由硬件完成以下功能: 
(1）根据响应的中断源的中断优先级, 使相应的优先级状态触发器置 1; 
(2）执行硬件中断服务子程序调用, 并把当前程序计数器PC的内容压入堆栈;
(3）清除相应的中断请求标志位（串行口中断请求标志 RI和 TI除外）; 
(4）把被响应的中断源所对应的中断服务程序的入口地址（中断矢量）送入PC, 从而转入相应的中断服务程序。
表  中断服务程序入口地址表👇
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507165241202.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
例如, 现有外部中断 1 提出申请, 且主程序中有R0、 R1、
DPTR、累加器A需保护, 则编制程序应为: 
ORG 0000H 
AJMP MAIN 
ORG 0013H 
LJMP INT1 …
ORG 0100H 
MAIN: …; 主程序 …
ORG 1000H


INT1: 
PUSH ACC ; 中断服务程序 
PUSH DPH 
PUSH DPL 
PUSH 0 
PUSH 1
…
POP 1 
POP 0 
POP DPL 
POP DPH 
POP ACC 
RETI


编程中应注意: 
(1） 在 0000H放一条跳转到主程序的跳转指令, 这是因为MCS-51单片机复位后, PC的内容变为 0000H, 程序从 0000H 开始执行, 紧接着 0003H是中断程序入口地址, 故在此中间只能 插入一条转移指令; 
(2） 响应中断时, 先自动执行一条隐指令“LCALL 0013H”, 而 0013H至 001BH（定时器 1 溢出中断入口地址）之间可利用的存储单元不够, 故放一条无条件转移指令。
(3） 在中断服务程序的末尾, 必须安排一条中断返回指令RETI, 使程序自动返回主程序。
## 5.3 中断系统的应用
5.3 中断系统的应用
例 1 单步操作的中断实现。 把一个外部中断（设为INT0]）设置为电平激活方式。 
其中断服务程序的末尾写上如下几条指令: 
JNB P3.2, $ ; 在INT0变高前原地等待(死循环) 
JB P3.2, $; 在 INT0变低前原地等待(死循环) 
RETI; 返回并执行一条指令

现在,若INT0保持低电平, 且允许INT0中断, 则CPU就进入外部中断 0 服务程序, 由于有上述几条指令, 它就会停在 JNB 处, 原地等待。当INT0 端出现一个正脉冲（由低到高, 再到低）时, 程序就会往下执行, 执行RETI后, 将返回主程序, 往下执行一条指令, 然后又立即响应中断,以等待INT0端出现的下一个正脉冲。 这样在INT0端每出现一个正脉冲, 主程序就执行一条指令, 实现了单步执行的目的, 要注意的是, 这个正脉冲的高电平持续时间不小于 3个周期, 以确保CPU能采集到高电平值。

例 2 多中断源。 
MCS - 51 单片机有两个外部中断输入端, 当有 2 个以上中断源时, 它的中断输入端就不够了。此时, 可以采用中断与查询相结合的方法来实现。 可以使每个中断源都接在同一 个外部中断输入端上, 同时利用输入口线作为多中断源情况 下各中断源的识别线。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507170001625.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
ORG 0003H 
LJMP INT0 …
INT0: 
PUSH PSW 
PUSH ACC 
JB P0.7, DV1 
JB P0.6, DV2 
JB P0.5, DV3 
JB P0.4, DV4
GOBACK: 
POP ACC 
POP PSW 
RETI 
DV1: … ; 装置1中断服务程序
…

---

开关S1和S2分别接至INT0和INT1，
初始时LED指示灯L1和L2熄灭，
当S1按下S2断开，L1亮，L2灭；
当S2按下S1断开，L2亮，L1灭。
用中断方式实现。编写程序

ORG 0000H
AJMP MAIN

ORG 0003H
LJMP INT0
ORG 0013H
LJMP INT1

MAIN:
MOV IE,#85H；让EX0,EX1为1，启动中断
SETB P0.0
SETB P0.1

INT0:
MOV SP,#50H
JMP SAVE
CLR P0.0
SETB P0.1
JMP BACK
RET1

INT1:
MOV SP,#70H
JMP SAVE
CLR P0.1
SETB P0.0
JMP BACK
RET1

SAVE:
SETB RS0;对Ri存储区的保护
SETB RS1
PUSH ACC
PUSH DPH;对DPTR的保护
PUSH DLH
PUSH B

BACK:
CLR RS0
CLR RS1
POP B
POP DLH
POP DPH
POP ACC
POP PSW

END

---
# 第6章 MCS - 51单片机内部定时器/ 计数器及串行接口
## 6.1 定时器/计数器的结构及工作原理 
### 6.1 定时器/计数器的结构及工作原理
图 6.1 定时器/计数器结构框图
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200513144721258.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
加法计数器是计满溢出时才申请中断, 所以在给计数器赋初值时, 不能直接输入所需的计数值, 而应输入的是计数 器计数的最大值与这一计数值的差值, 设最大值为 M, 计数 值为 N, 初值为 X, 则 X的计算方法如下:
计数状态: X=M－N <计数外部给的信号>
定时状态: X=M－定时时间/T <内部时钟信号>
而T=12÷晶振频<常选晶振频率11.0592Mhz>
### 6.2 方式和控制寄存器
#### 一、定时器/计数器的方式寄存器TMOD
图 6.2 TMOD各位定义
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200513150048510.png)
##### 1. M1M0工作方式控制位
表 6.1 工作方式选择表
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200513150635959.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
##### 2. C/T定时器方式或计数器方式选择位
若C/T=1时, 为计数器方式; C/T = 0时, 为定时器方式。
##### 3. GATE 定时器/计数器运行门控标志位 
当GATE=1时, 只有INT0 (或INT1)引脚为高电平且TR0(或TR1 )置 1 时, 相应的定时器 /计数器才被选通工作, 这时可用于测量在INTx端出现的正脉冲的宽度。若GATE=0, 则只要 TR0 (或 TR1)置 1, 定时器 /计数器就被选通, 而不管 INT0 (或 INT1)的电平是高还是低
#### 二、定时器/计数器控制寄存器TCON
**TF0、TF1分别是定时器/计数器T0、 T1 的溢出标志位**, 加法计数器计满溢出时置 1, 申请中断, 在中断响应后自动复 0。
TF产生的中断申请是否被接受, 还需要由中断是否开放来决定。 
**TR1、TR0 分别是定时器 /计数器T1、 T0 的运行控制位**,通过软件置 1 后, 定时器 /计数器才开始工作, 在系统复位时被清 0。
### 6.3 工作方式
#### 一、方式 0
图 6.4 方式 1（16位计数器）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200513155010611.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
#### 二、方式 1
图 6.4 方式 1（16位计数器）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200513155641882.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
#### 三、方式 2
图 6.5 方式 2（初始常数自动重装载）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200513155701669.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
另一个八位置有初值，自动重新装载

#### 四、方式 3 
图 6.6 方式 3（两个 8 位独立计数器）
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020051315573897.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
T1去串行口相关工作位置

## 6.4 定时器/计数器应用举例
### 一、方式 0 的应用例 1 利用定时器输出周期为 2 ms的方波, 设单片机晶振频率为 6 MHz。
选用定时器 /计数器T0 作定时器, 输出为P1.0 引脚, 2 ms 的方波可由间隔 1 ms的高低电平相间而成, 因而只要每隔 1 ms对 P1.0 取反一次即可得到这个方波。
定时 1 ms的初值: 
因为机器周期=12÷6 MHz= 2 μs
所以 1 ms内T0需要计数N次: N= 1 ms÷2 μs = 500
## 6.5 MCS - 51单片机的串行接口
## 6.6 串行口的应用





## 5. 算数运算类指令
## 6. 逻辑操作类指令
## 7. 控制转移类指令
## 8. 位操作类指令



# 第三章 第一个单片机系统

录
  - 如何控制一个发光二极管——闪烁 500ms
  -  

![发光二极管电路图](https://img-blog.csdnimg.cn/20200412180808821.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)
![电路描述1](https://img-blog.csdnimg.cn/20200412181420119.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hxX2ZhbGxpbmc=,size_16,color_FFFFFF,t_70)

