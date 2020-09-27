## oh my zsh的安装

​	看了很多教程发现都是使用如下语句进行安装

```text
# via curl sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

但是实践过后会发现，因为某些原因会出现连接失败，下载不成功。

**我们可以使用如下方式进行替代：**

1. 在 **[oh-my-zsh](https://link.zhihu.com/?target=https%3A//github.com/ohmyzsh/ohmyzsh)** GitHub上下载zip

2. 对下载下来的对象进行**解压**

3. ```
	cd ~/Downloads //进入下载目录，解压文件所在的地方
	mv ohmyzsh-master ~/.oh-my-zsh	//移动 oh-my-zsh 目录到根目录
	cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc	//把 .zshrc 配置文件拷贝到根目录下
	source ~/.zshrc //设置环境变量
	```

4. 重启item2。



参考文章：https://zhuanlan.zhihu.com/p/145437836

