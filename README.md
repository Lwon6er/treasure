# treasure
something about FPGA

20251223 23:58:30 
  电机控制模块划分：
      1.如何从机械角度换算出电角度 （重点）;
      2.ADC采集电流;
      3.clark变换和park变换;
      4.逆park变换;
      5.SVPWM发生器;
      6.ADC采集电流的时间;

20251225 19:43:50
  一、如何从机械角度换算出电角度
  当前电机参数<img width="435" height="1035" alt="d3a433b8-2171-4a75-9f0b-930134568ad9" src="https://github.com/user-attachments/assets/5803f138-9f3c-49ee-9ebb-cce459e7054b" /> ，我们可以得知的信息：
  1.电机带有2500PPR增量式反馈原件
  2.电机极对数=5

  二、分析
  1.编码器信号输出波形和电平标准（待测量）
  2.增量式编码器A/B/Z的工作原理
    <img width="850" height="436" alt="ad779304-df5c-4b2e-88da-69773f35a9f8" src="https://github.com/user-attachments/assets/01f8ca09-a087-45e5-918f-787042a6e1a9" />
    使用发光二极管发射，圆盘上有等间距透明部分，光电探测器发送脉冲。
  3.使用FPGA管脚直接接收信号还是ADC采集后再输入FPGA
    A/B/Z信号是脉冲时，选择直接输入FPGA；正/余弦信号时，选择ADC采集后输入FPGA，可细分，精度高。

  三、待办事项
  1.给电机上电，手动转动电机，用示波器观察编码器信号。编码器接口定义如下：
  <img width="1856" height="780" alt="image" src="https://github.com/user-attachments/assets/0599eb0b-e523-4e69-879b-409c7b83873a" />

20251229 21:58:56
  一、再次梳理所有要学习的知识
  1.1 电机原理部分：dq电压方程。了解参数的含义
  1.2 FOC电流环控制
  1.3 速度环/位置环串级整定
  1.4 编码器位置/速度解析
  1.5 控制系统理论
  二、三相电路
  2.1.知识记录
  三相电路由三相电源，三相负载和三相输电线组成。
  对称三相电源：三个频率相同，振幅相同，相位彼此相差120°的正弦电源。通常由三相同步发电机产生，三相绕组在空间相差120°，当转子以均匀角速度旋转时，在三相绕组形成感应电压，从而形成三相电源。<img width="591" height="591" alt="image" src="https://github.com/user-attachments/assets/d731fb4c-bf9e-4876-9a90-3440b46fd79d" />
  三、clark算法的原理
  https://zhuanlan.zhihu.com/p/172484981
  问题1:三相电流的表达式？  
  问题2:等幅值和等功率有什么区别？
  问题并没有得到有效的解答，所以我决定先看《电路原理》的三相电路部分。
  










  
