![image](https://github.com/jdbwlj/hassio-zigbee2mqtt-1/blob/master/zigbee2mqtt/logo-cangji.jpg)

# Home Assistant Add-on: Zigbee2MQTT-1

![image](https://github.com/jdbwlj/hassio-zigbee2mqtt-1/blob/master/zigbee2mqtt/%E6%AD%A3%E7%A1%AE%E4%BF%AE%E6%94%B9%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6%E6%96%B9%E5%BC%8F.png)

MQTT:
```shell
base_topic: zigbee2mqtt1
#base_topic多加一个1 区分多开主题
server: mqtt://localhost:1883
#mqtt在Home Assistantaz 安装，localhost是Home Assistantaz的ip,端口1883
user: mqtt
password: mqtt
client_id: zigbee2mqtt1
#client_id多加一个1 区分多开mqtt客户端id
```

serial:
```shell
adapter: ezsp
port: tcp://[Gateway_IP]:[Port]
#多模和企业版端口8888 多模自动版端口6638
#多模自动版域名: port: tcp://tube-zb-gw-efr32-xxxxxx.local:6638 
```

channel:
```shell
advanced:
  channel: 15
  #信道要分开 防止干扰 选15 20 25
  #z2m网页UI设置步骤z2m设置→高级→ZigBee channel
```
