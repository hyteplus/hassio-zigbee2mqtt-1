# Home Assistant Add-on: Zigbee2MQTT-1

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
