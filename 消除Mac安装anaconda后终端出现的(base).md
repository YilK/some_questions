## 消除Mac安装anaconda后终端出现的(base)

打开终端输入

```zsh
vi ~/.condarc
```

然后在文件中输入

```zsh
changeps1: False
```

然后进行保存退出。

重启终端，可以发现(base)字段消失了。



参考博客：https://www.jianshu.com/p/6cdc9713c4ed

