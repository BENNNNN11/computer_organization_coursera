计算机基本结构

1. **冯诺依曼结构**

    1. 程序存放在存储器中
    2. 二进制
    3. **运算器CA，控制器CC， 存储器M**，输入/输出设备I/O
        1. **运算器+控制器=cpu**
        2. **存储器 = 主存**
        3. **cpu和主存通过系统总线连接**
        4. **主存的组织形式： 地址（二进制）+内容（连续编号）**
    4. 最初的微处理器： Intel 4004 

2. **计算机简化模型（模型机）**： 

    1. **CPU**：
        1. **控制器**：取，分析和执行指令
            - **指令寄存器：instruction register(IR)** 用来存放正在执行或者即将执行的指令
            - **程序计数器program counter(PC)**：存放下一条指令的存储单元地址
            - **存储器地址寄存器 MAR**
            - **存储器数据寄存器 MDR**
            - **指令译码部件**: 对IR中的指令进行译码，以确定IR 中存放的是哪一条指令
            - **控制电路**: 产生控制信号，在时序脉冲的同步下控制各个部件的动作
        2. **运算器**：算数运算和逻辑运算
            - **ALU**: 算术逻辑运算单元
            - **通用寄存器R0-Rn-1**：
            - **内部总线**： 用于cpu内部各个部件之间传递数据
    2. **存储器**：
        - **位宽**由**编址方式**确定： 
            - **按字节编址**，每一个存储单元能存放八位二进制数，每个存储单元的地址也是唯一的
        - **MAR**(memory address register): 存储器地址寄存器：用来存放CPU正在读写的存储单元的地址
        - **MDR**(memory data register): 存储器数据寄存器： 用来存放cpu正在读出或即将写入存储单元的数据
    3. **系统总线**：
        1. **数据总线**：宽度一般为位宽的整数倍
        2. **地址总线：**如果地址总线的宽度为n，则cpu能管理的存储单元为2^n个。
        3. **控制总线**：与存储器中的控制逻辑相连，用来接受cpu的读写信号，或者向cpu反馈传输已完成的信号。

3. **计算机执行指令的过程**： 

    1. **计算机完成指令的步骤**： 

        **取址fetch->译码decode->执行execute->回写write-back**

    2. 示例： 
        - **ADD R0, [6]** 
        - **通用寄存器r0的内容  + 地址为6的存储单元的值， 然后更新到r0中**
    3. **取址**： 
        - **控制器将指令的地址送往存储器**
        - **存储器按给定的地址读取指令内容，送回控制器**
    4. **译码：控制器分析指令性质，并向有关部件发出指令信号。**
    5. **执行**：**从通用寄存器或存储器中取出操作数，并命令运算器对操作数进行指令规定的运算。**
    6. **回写**

4. **计算机的输入和输出**： 

    1. 穿孔纸带
    2. 电传打字机
    3. 硬盘

5. 

    

