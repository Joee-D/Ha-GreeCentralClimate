# Ha-GreeCentralClimate
格力中央空调Homeassistant插件，使用格力云控进行控制

方式1：greeCentral目录复制到custom_components，再在configuration.yaml中加上配置：
```
climate:
  - platform: greeCentral
```
方式2：
支持通过HACS自定义集成
![image](https://user-images.githubusercontent.com/32849562/162217206-37b7da25-f0af-4ba9-9e0d-85f967e0388c.png)
![image](https://user-images.githubusercontent.com/32849562/162217652-5399b5e5-6c2d-4ab5-a809-06e9b41f3789.png)

1.温度传感器
请修改climate.py 65行
TEMP_SENSORS = {'48218b1b000000': 'sensor.4c65a8dac083_temperature', '0a188a1b000000': 'sensor.48574300bf12_temperature','1c638b1b000000': 'sensor.0x158d000632c092_temperature'}
第一个是分机的MAC，第二个是想要绑定的传感器实体ID，后续考虑做成通过配置文件或者界面……



# 参考
[Ha-GreeCentralClimate](https://github.com/xcy1231/Ha-GreeCentralClimate)

[gree-hvac-mqtt-bridge](https://github.com/arthurkrupa/gree-hvac-mqtt-bridge)

[HomeAssistant-GreeClimateComponent](https://github.com/RobHofmann/HomeAssistant-GreeClimateComponent)

[[插件发布] [5月6日更新]带反馈的WIFI空调](https://bbs.hassbian.com/forum.php?mod=viewthread&tid=3651)
