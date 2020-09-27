## 解决ROS中每次都要设置环境变量的问题

在编译完工作工作空间之后，需要设置环境变量

```
$ source devel/setup.bash
```

为了解决每次都需要重新设置环境变量这个问题，可以采取如下方法。

### 1.按ctrl+h显示出隐藏文件

### 2.找到.bashsrc文件并打开

### 3.在最后面一行写上

```
source /home/用户名/catkin_ws(自己的工作空间)/devel/setup.bash
```

