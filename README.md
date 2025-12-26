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











  
