---
id: setup-ros
sidebar_position: 2
title: ROS环境搭建
---

# ROS环境搭建

## 下载ROS
:::tip 下载小建议
  
推荐使用鱼香ROS一键安装

:::

[鱼香ROS](https://fishros.org.cn/forum/topic/20/%E5%B0%8F%E9%B1%BC%E7%9A%84%E4%B8%80%E9%94%AE%E5%AE%89%E8%A3%85%E7%B3%BB%E5%88%97)
  
一键安装指令  
```bash
wget http://fishros.com/install -O fishros && . fishros
```
安装选择ROS1 Melodic桌面完整版  

## 设置ROS环境变量
将环境变量添加进bash中  
```bash
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc
``` 

如果安装了多个 ROS 发行版，~/.bashrc必须只为你当前使用的版本提供setup.bash。  

如果您只想更改当前 shell 的环境，则可以输入：  
```bash
source /opt/ros/melodic/setup.bash
```  

## 构建包的依赖
到目前为止，已经安装了运行核心 ROS 包所需的东西。要创建和管理你自己的 ROS 工作区，有各种单独分发的工具和要求。例如，rosinstall是一种常用的命令行工具，它使您可以通过一个命令轻松下载 ROS 包的许多源代码树。  
要安装此工具和其他用于构建 ROS 包的依赖项，运行：  
```bash
sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
```
初始化rosdep:  
```bash
sudo rosdep init
rosdep update
```  
