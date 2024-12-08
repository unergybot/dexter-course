---
sidebar_position: 3
---

# 设置GLUON应用软件

本文档以GLUON桌面型六轴机械臂为例，展示如何连接机械臂，以及在PC端运行ROS的过程。

## 创建工作目录
开启终端，执行以下命令
```bash
sudo apt-get update
mkdir -p catkin_ws/src
cd catkin_ws/src
```
## 克隆GLUON应用软件包
```bash
git clone https://github.com/mintasca/ros_gluon.git
```
::: tip[如果没安装git,请先安装git]
```bash
sudo apt-get install git
```
:::

```bash
cd ..
git clone https://github.com/innfos/innfos-cpp-sdk.git
cp –r innfos-cpp-sdk/sdk src/ros_gluon/gluon/ActuatorController_SDK
cp –r innfos-cpp-sdk/sdk src/ros_gluon/gluon_control/ActuatorController_SDK
```

## 安装依赖包并编译
```bash
sudo apt-get install ros-melodic-ros-control-boilerplate
sudo apt-get install ros-melodic-moveit-visual-tools
sudo apt-get install ros-melodic-moveit
sudo apt-get install ros-melodic-joint-state-publisher-gui
sudo apt-get install ros-melodic-ros-controllers

cd catkin_ws
catkin_make
```

## 配置运行环境
```bash
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

:::tip[注意]

这个操作只需一次操作，重新开启Terminal 终端窗口时自动设置。

:::