## macOS(版本10.15.6)下下载anaconda并在pycharm中使用

### 第一步	下载

在清华大学镜像站中找到自己想下载的版本
地址：https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/
我下载的是：[Anaconda3-2020.07-MacOSX-x86_64.pkg](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/Anaconda3-2020.07-MacOSX-x86_64.pkg)

### 第二步	安装

安装anacodna,仅在此电脑上安装,按照默认步骤安装即可。

### 第三步	检查

检查是否安装成功，打开终端输入conda 出现如下信息表示成功

```
usage: conda [-h] [-V] command ...
conda is a tool for managing and deploying applications, environments and packages.
Options:
positional arguments:
  command
    clean        Remove unused packages and caches.
    config       Modify configuration values in .condarc. This is modeled
                 after the git config command. Writes to the user .condarc
                 file (/Users/yilk/.condarc) by default.
    create       Create a new conda environment from a list of specified
                 packages.
    help         Displays a list of available conda commands and their help
                 strings.
    info         Display information about current conda install.
    init         Initialize conda for shell interaction. [Experimental]
    install      Installs a list of packages into a specified conda
                 environment.
    list         List linked packages in a conda environment.
    package      Low-level conda package utility. (EXPERIMENTAL)
    remove       Remove a list of packages from a specified conda environment.
    uninstall    Alias for conda remove.
    run          Run an executable in a conda environment. [Experimental]
    search       Search for packages and display associated information. The
                 input is a MatchSpec, a query language for conda packages.
                 See examples below.
    update       Updates conda packages to the latest compatible version.
    upgrade      Alias for conda update.

optional arguments:
  -h, --help     Show this help message and exit.
  -V, --version  Show the conda version number and exit.

conda commands available from other packages:
  build
  convert
  debug
  develop
  env
  index
  inspect
  metapackage
  render
  server
  skeleton
  verify
```

### 第四步 pycharm中使用anaconda

打开pycharm，点击 new project，在pure python 中进行如下图所示的设置（在New environment using 使用conda之后，下面的路径会自动填好不需要手动输入），最后点击Creat。

<img src="/Users/yilk/Desktop/截屏2020-08-18 上午9.20.01.png"  />

### 第五步 Hello World

​	easy。

