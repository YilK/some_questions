## 安装ROS

### 1.打开软件与更新

​	勾选关键字 universe restricted multiverse 设置国内的下载源

### 2.添加sources.list

```
$ sudo sh -c '. /etc/lsb-release && echo "deb http://mirrors.ustc.edu.cn/ros/ubuntu/ $DISTRIB_CODENAME main" > /etc/apt/sources.list.d/ros-latest.list'
```

这一步配置将镜像添加到Ubuntu系统源列表中，建议使用国内或镜像源，这样能够保证下载速度。本例使用的是中国科技大学的源。

### 3.添加keys

```
$ sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
```

公钥是Ubuntu系统的一种安全机制，也是ROS安装中不可缺的一部分。

### 4.系统更新

```
$ sudo apt-get update && sudo apt-get upgrade
```

更新系统，确保自己的Debian软件包和索引是最新的。

### 5.安装ROS

Ubuntu 16.04安装Kinetic版本

```
$ sudo apt-get install ros-kinetic-desktop-full # Ubuntu 16.04
```

### 6.配置ROS

1.初始化rosdep

```
$ sudo rosdep init && rosdep update
```

可能会出现连接不上的情况。

```
$sudo gedit /etc/hosts
```

在末行加入

```
199.232.28.133 raw.githubusercontent.com
```

2.ROS环境配置

```
#For Ubuntu 16.04
$ echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
```

**注意：** ROS的环境配置，使得你每次打开一个新的终端，ROS的环境变量都能够自动配置好，也就是添加到bash会话中，因为命令`source /opt/ros/kinetic/setup.bash` 只在当前终端有作用，即具有单一时效性，要想每次新开一个终端都不用重新配置环境，就用echo语句将命令添加到bash会话中。

3.安装rosinstall

[rosinstall](http://wiki.ros.org/rosinstall) 是ROS中一个独立分开的常用命令行工具，它可以方便让你通过一条命令就可以给某个ROS软件包下载很多源码树。在ubuntu上安装这个工具，请运行：

```
$ sudo apt-get install python-rosinstall
```

