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
