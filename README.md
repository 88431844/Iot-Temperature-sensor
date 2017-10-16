# IotSensor

## 硬件基于esp8266 和 传感器的物联网设备

软件基于物联网MQTT协议，连接到MQTT broker(server),每隔一段时间进行数据上报

预计开发：

Iot-Temp:基于 esp8266-01 和 ds18b20 温度传感器的温度物联网设备，按照一定时间间隔上传温度数据到broker。

Iot-Humidity:基于 esp8266-01 和 DHT11 湿度传感器的物联网设备，按照一定时间间隔上传湿度数据到broker。

Iot-Socket:基于esp8266-01 和 led、继电器、按钮的插座的物联网设备，led用于显示开关状态，按钮用于切换开关状态，继电器用于接通、切断电源。

Iot-Reed:基于esp8266-01 和 干簧管、磁铁的门窗状态物联网设备。

设计目标：

1.WiFi配置：

默认没有设置WiFi，进入AP模式；
手机会搜到一个定义好的WiFi名称（例如：esp-temp01,可能根据以后定义规则生成随机序列号）
连接后，可以搜索可以连接的WiFi列表，也可以直接输入WiFi名称，和密码进行连接。

2.MQTT相关配置

通过配置WiFi页面，设置设备topic（用于别人订阅设备上报数据），client（用于识别设备），以及上报时间（可能是下拉选择，5,10,15秒这种）
以及broker的ip和端口

3.节能模式

如果设备上传时间较长，比如五分钟上报一次，则设备可以进入深度睡眠，达到省电目的，因为未来可能做成以CR2032供电




