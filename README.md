# Ha-GreeCentralClimate
格力中央空调Homeassistant插件，使用格力云控进行控制
![image](https://user-images.githubusercontent.com/32849562/162439309-53d0ea12-2bcc-443d-933e-b08167a2b0c1.png)


## 方式1：greeCentral目录复制到custom_components
## 方式2：支持通过HACS自定义集成

在config下创建customize.yaml（后续会用到）
在config下创建climate.yaml
```
- platform: greeCentral
```
再在configuration.yaml中加上配置：
```
climate: !include climate.yaml
homeassistant:
  customize: !include customize.yaml
```

首次启动后，会自动生成对应的空调实体，可以获得空调实体id
![image](https://user-images.githubusercontent.com/32849562/162438731-84e79361-40d4-452a-a0ec-a4c775b50045.png)
在customize.yaml中新增配置
```
空调实体ID:
  温度传感器实体ID
climate.ge_li_kong_diao_48218b1b000000:
  temp_sensor: sensor.2c116522c3ef_temperature
climate.ge_li_kong_diao_0a188a1b000000:
  temp_sensor: sensor.8cf6819b6e92_temperature
climate.ge_li_kong_diao_1c638b1b000000:
  temp_sensor: sensor.2c11651e9299_temperature
```
# 参考
[Ha-GreeCentralClimate](https://github.com/xcy1231/Ha-GreeCentralClimate)

[gree-hvac-mqtt-bridge](https://github.com/arthurkrupa/gree-hvac-mqtt-bridge)

[HomeAssistant-GreeClimateComponent](https://github.com/RobHofmann/HomeAssistant-GreeClimateComponent)

[[插件发布] [5月6日更新]带反馈的WIFI空调](https://bbs.hassbian.com/forum.php?mod=viewthread&tid=3651)
