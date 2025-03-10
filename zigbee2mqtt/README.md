# Home Assistant Add-on: Zigbee2MQTTA

<div align="center">
    <div style="display: flex;">
        <a href="https://github.com/zigbee2mqtt/hassio-zigbee2mqtt/actions?query=workflow%3ACI">
            <img src="https://github.com/zigbee2mqtt/hassio-zigbee2mqtt/workflows/CI/badge.svg">
        </a>
        <a href="https://github.com/zigbee2mqtt/hassio-zigbee2mqtt/releases">
            <img src="https://img.shields.io/github/release/zigbee2mqtt/hassio-zigbee2mqtt.svg">
        </a>
        <a href="https://github.com/zigbee2mqtt/hassio-zigbee2mqtt/stargazers">
            <img src="https://img.shields.io/github/stars/zigbee2mqtt/hassio-zigbee2mqtt.svg">
        </a>
        <a href="https://discord.gg/dadfWYE">
            <img src="https://img.shields.io/discord/556563650429583360.svg">
        </a>
        <a href="http://zigbee2mqtt.discourse.group/">
            <img src="https://img.shields.io/discourse/https/zigbee2mqtt.discourse.group/status.svg">
        </a>
    </div>
    <p>
<a href="https://www.gpio.club/">藏机官网</a> 点击跳转。</p>
</div>

MQTT:
```shell
base_topic: zigbee2mqttA
#base_topic多加一个A 区分多开主题
server: mqtt://localhost:1883
#mqtt在Home Assistantant 安装，localhost是Home Assistantant的ip,端口1883
user: mqtt
password: mqtt
client_id: zigbee2mqttA
#client_id多加一个1 区分多开mqtt客户端id
```

serial:
```shell
adapter: ebmer
port: tcp://[Gateway_IP]:[Port]
```

channel:
```shell
advanced:
  channel: 15
  #信道要分开 防止干扰 选15 20 25
  #z2m网页UI设置步骤z2m设置→高级→ZigBee channel
  #删除zigbee2mqtt文件夹下coordinator_backup.json和state.json解决信道报错
```
