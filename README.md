# 参考资料

1. https://oshwhub.com/msraphael/FE2.1fang-an-yan-zheng-ban
2. https://oshwhub.com/klshu36/usb-hub

# 功能需求

1. 可使用外部供电功能，具有过流保护，1A
2. 每个接口都有ESD保护

# FE2.1芯片数据手册阅读

USB2.0传输芯片，最高传输速率约为480Mbps，实际有效传输速率约为20Mbps。

一路上行通道接入电脑，7路下行通道接入U盘、鼠标等外部设备。

FE2.1通过外部5V进行供电，其内部自动将电压转化为3.3V、1.8V供不同的模块使用。

引脚定义说明：

1. 2号引脚TESTJ可用于读取外围芯片EEPROM的数据内容
2. 22、23引脚外界12M晶振
3. 27引脚外接2.7K电阻，用于调节芯片内部的电源
4. **40引脚接外部复位电路，一般使用“阻容复位电路”，来实现芯片的上电复位。**
5. 41引脚用于检测芯片是否接入上位机
6. 45、43引脚可用于检测第1、5下行通道是否过流
7. 44引脚用于指示电源状态的使能信号



# USB hub设计注意事项

