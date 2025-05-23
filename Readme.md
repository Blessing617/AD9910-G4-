/**
  ******************************************************************************
  * @user           : Blessing(songfu)
  * @time           : 2025.4.4
  * @Keil5          : pVision V5.38.0.0
  * @STM32CubeMX    : Version 6.9.2
  ******************************************************************************
  * @Description
  * AD9910 DDS信号发生器驱动程序实现和移植,使用STM32G474RE单片机实现与模块的spi串行通信.
  *
  * @IO
  * 硬件串口            PC4 -> USART1_TX  PC5 -> USART1_RX
  *
  * @Attention
  * 频率范围: 1Hz-420MHz(正弦波)
  * 输出波形: 正弦波,三角波,方波,SINC波等
  * 输出幅度: 正弦波760mVpp(max),含直流,随频率衰减
  * 输出相位: 两路差180度输出
  *
  * @模块接线
  * AD9910模块        STM32G474RE
  *      DC    <------  5.0V      5V供电
  *      GND   -------  GND       地
  *      RST   <------  PA6       复位信号
  *      PWR   <------  PA7       掉电控制
  *      DRC   <------  PB6       数字斜坡控制
  *      DRH   <------  PC7       数字斜坡保持
  *      SDIO  <----->  PA9       串行数据输入输出
  *      SCLK  <------  PA8       时钟信号
  *      CS    <------  PB10      片选信号+通信复位
  *      PF0   <------  PB4
  *      PF1   <------  PB5
  *      PF2   <------  PB3       Profile选择引脚
  *      UP    <------  PA10      同步信号
  *
  * OLED模块(软件IIC)  STM32G474RE
  *      VCC   <------  5.0V      5V供电
  *      GND   -------  GND       地
  *      SCL   <------  PB9       IIC时钟线
  *      SDA   <----->  PB8       IIC数据线
  ******************************************************************************
  */
