# 坦克车底盘驱动

底盘包括imu和电机的相关驱动。
详细的文档以及接口说明，[https://github.com/ykevin/rikirobot_docs](https://github.com/ykevin/rikirobot_docs)

### rosnode 说明

#### arduino_serial_node
读取驱动板上的数据并发布，控制电机
```
/battery # 显示电池电压(V)
/cmd_vel # 订阅Twist消息
/diagnostics # 显示错误信息
/pid # 不知道
/raw_imu # 发布原始imu数据
/raw_vel # 发布原始轮速
```

#### imu_calib
GY-85（九轴）：

#### imu_filter_madgwick
imu滤波节点

#### base_footprint_to_imu_link