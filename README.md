# [BluePowerRobotics](https://BluePowerRobotics.github.io)

以下是所有人必修内容。

目录在[这里](#其他内容)

## 所有人必修

| Control Hub | Expansion Hub | Driver Hub | REV SLIM ROBOT BATTERY |
|---|---|---|---|
| ![Control Hub](/RES/ControlHub.png) | ![Expansion Hub](/RES/ExpansionHub.png) | ![Driver Hub](/RES/DriverHub.png) | ![Rev Slim Robot Battery](/RES/Battery.png) |
| 机器人核心部件，用于控制各个执行器（电机、舵机）及传感器（可用手机+EXPANSION HUB代替）。需要使用电池供电；USB-typeC口不可（给CONTROL HUB）供电。 | 用于拓展控制，增加可用舵机、电机数。对于FTC，一辆车最多接12舵机、8电机，因此对于CONTROL HUB只需要且仅允许接入1个EXPANSION HUB（通过RS485接口或MINI USB接口连接） | 连接车辆以执行程序。通过其中Driver Station软件启动。（可用手机代替）使用手柄操控。通过Start+A/B切换第一/二操作手。该软件界面左下部分控制程序运行。该部分顶端显示当前使用程序；按右侧向下三角切换。 | 机器人电源，为设备供电。镍氢电池，无3C标志，并非充电宝，不受新规限制，可以随身携带上飞机。标称电压12V，是12个1.2V电芯串联组成。本身装有（可在国内买到的）保险丝。 |

| 电机 | （普通）舵机 |
|---|---|
| ![REV HD HEX MOTOR](/RES/HdHexMotor.jpg) ![Go Bilda Yellow Jacket Motor](/RES/YellowJacketPlanetaryGearMotor.jpg) | ![DSSERVO](/RES/DSSERVO.png) ![TIANKONGRC](/RES/TIANKONGRC.png) |
| 通过两种线与机器人控制核心连接。电源线提供动力（黑/红），Encoder线获取旋转圈数（红蓝黑白）。特别地，对于Go Bilda电机，均需要特制转接线；这些线应当在购买时与电机配套。如果需要安装在难以拆卸/接线的位置（虽然不建议这么做），请提前将这两种线接好、拉到易于连接的地方。 | （又称为伺服电机）通过三根线（黑/红/白 或 褐/橙/黄）与机器人控制核心连接。对于180、270舵机，信号线（白或黄）向舵机传输角度；对于360舵机，信号线（白或黄）向舵机传输其旋转速度。若想要控制360舵机角度，可考虑磁传感。特别地，无论是何种范围的控制角度舵机，其实际可用角度大概率小于其标定角度：如170/180，255/270。不建议直接通过控制其旋转时间来间接控制角度。需要注意的是，若想要提高效率，工程部成员应当在安装舵机的时候请程电部成员测试/控制其初始角度而非自做主张安装。 |

## 其他内容

- [机械程序与电子设计(程电)](/ProgTeam/README.md)

- [机械动力设计制造(工程)](/EngiTeam/README.md)

- [商业宣传与外交联络(商宣)](/BusiTeam/.README.md)