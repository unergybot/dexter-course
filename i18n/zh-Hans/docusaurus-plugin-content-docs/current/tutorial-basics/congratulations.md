---
sidebar_position: 5
---

# 常见问题

## 环境准备可能遇到的问题
### Curl not found
```bash
sudo apt-get install curl
```

### catkin_make not found
首先检查是否正确安装ros melodic，其次检查是否正确配置source 环境变量至.bashrc 或执行了相关source操作，如果前两步已经操作请尝试重启Terminal 终端窗口。 

## 编译时常见问题

### Could NOT find ros-control-boilerplate
```bash
sudo apt-get install ros-melodic-ros-control-boilerplate
```

### Could NOT find moveit_core
```bash
sudo apt-get install ros-melodic-moveit-core
```

### Could NOT find moveit_ros_planning_interface
```bash
sudo apt-get install ros-melodic-moveit-ros-planning-interface
```

### Could NOT find moveit_ros_perception
```bash
sudo apt-get install ros-melodic-moveit-ros-perception
```

### fatal error: actuatorcontroller.h
```bash
cd catkin_ws
cp –r innfos-cpp-sdk/sdk  src/ros_gluon/gluon/ActuatorController_SDK/
cp –r innfos-cpp-sdk/sdk  src/ros_gluon/gluon_control/ActuatorController_SDK/
```
innfos-cpp-sdk 下载请参考源码下载

## 运行时常见错误
### Could not find the GUI, install the 'joint_state_publisher_gui' packag
```bash
sudo apt-get install ros-melodic-joint-state-publisher-gui
```

### Exception while loading controller manager 'moveit_simple_controller/MoveItSimpleControllerManager'
```bash
sudo apt-get install ros-melodic-moveit-simple-controller-manager
```

### Exception while loading planner 'ompl_interface/OMPLPlanner'
```bash
sudo apt-get install ros-melodic-moveit-planners-ompl
```

### PluginlibFactory: The plugin for class 'moveit_rviz_plugin/MotionPlanning’ failed to load'
```bash
sudo apt-get install ros-melodic-moveit-ros-visualization
```
### Connected error code: 803
这个错误是未检测到ECB，请检查是否正确连接机械臂及ECB至PC。