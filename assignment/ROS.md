###一、ROS介绍
ROS (Robot Operating System, 机器人操作系统) 提供一系列程序库和工具以帮助软件开发者创建机器人应用软件。它提供了硬件抽象、设备驱动、库函数、可视化、消息传递和软件包管理等诸多功能。ROS遵守BSD开源许可协议。
ROS 的主要目标是为机器人研究和开发提供代码复用的支持。ROS是一个分布式的进程（也就是“节点”）框架，这些进程被封装在易于被分享和发布的程序包和功能包中。ROS也支持一种类似于代码储存库的联合系统，这个系统也可以实现工程的协作及发布。这个设计可以使一个工程的开发和实现从文件系统到用户接口完全独立决策（不受ROS限制）。同时，所有的工程都可以被ROS的基础工具整合在一起。
###二、ROS安装步骤
####1.配置 Ubuntu 软件仓库
配置你的 Ubuntu 软件仓库(repositories) 以允许 "restricted"、"universe" 和 "multiverse"这三种安装模式。 你可以 按照[ubuntu中的配置指南](https://help.ubuntu.com/community/Repositories/Ubuntu)来完成配置。 
####2.添加 sources.list
配置你的电脑使其能够安装来自 packages.ros.org的软件包。 ROS Jade 仅支持Trusty (14.04)、Utopic (14.10) 和 Vivid (15.04)。
`sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'`
####3.添加 keys
`sudo apt-key adv --keyserver hkp://pool.sks-keyservers.net --recv-key 0xB01FA116`
####4.安装
首先，确保你的Debian软件包索引是最新的： 
`sudo apt-get update`
**桌面完整版安装：** 包含ROS、rqt、rviz、通用机器人函数库、2D/3D仿真器、导航以及2D/3D感知功能。 
`sudo apt-get install ros-jade-desktop-full`
####5.初始化 rosdep
在开始使用ROS之前你还需要初始化rosdep。rosdep可以方便在你需要编译某些源码的时候为其安装一些系统依赖，同时也是某些ROS核心功能组件所必需用到的工具。 
`sudo rosdep init`
`rosdep update`
####6.环境配置
如果每次打开一个新的终端时ROS环境变量都能够自动配置好（即添加到bash会话中），那将会方便很多： 
`echo "source /opt/ros/jade/setup.bash" >> ~/.bashrc`
`source ~/.bashrc`
如果你安装有多个ROS版本, ~/.bashrc
 必须只能 source 你当前使用版本所对应的 setup.bash
。 
如果你只想改变当前终端下的环境变量，可以执行以下命令： 
`source /opt/ros/jade/setup.bash`
####7.安装rosinstall
rosinstall是ROS中一个独立分开的常用命令行工具，它可以方便让你通过一条命令就可以给某个ROS软件包下载很多源码树。 
要在ubuntu上安装这个工具，请运行：
`sudo apt-get install python-rosinstall`
####8.检查ROS系统
输入以下指令进行检查：
`roswtf`
###三、ROS安装结果：
对安装好的ROS系统进行检查，可以得到以下结果：

![结果.png](http://upload-images.jianshu.io/upload_images/3250499-bc51277dc2711928.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
从结果看出，ROS系统已经成功安装且能够在ubantu上对其进行操作和调试。
