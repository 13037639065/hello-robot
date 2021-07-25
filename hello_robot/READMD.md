# 坦克车底盘驱动

底盘包括imu和电机的相关驱动。
详细的文档以及接口说明，[https://github.com/ykevin/rikirobot_docs](https://github.com/ykevin/rikirobot_docs)

### rosnode 说明

#### arduino_serial_node
读取驱动板上的数据并发布，控制电机

#### imu_calib
GY-85（九轴）：发布imu原始数据

#### imu_filter_madgwick
imu滤波节点

#### base_footprint_to_imu_link