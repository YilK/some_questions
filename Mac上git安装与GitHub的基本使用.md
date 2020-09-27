## Mac上git安装与GitHub的基本使用

### 1⃣️安装git

​	首先需要安装Homebrew，参考方法：https://zhuanlan.zhihu.com/p/111014448

​	在安装Homebrew是会提示让你安装git（如果你原先没有安装过，我的情况是这样的）

​	如果没有安装git的话，下载好Homebrew后，终端执行

```
brew install git
```

### 2⃣️设置SSH密钥

​	**1.创建一个新的SSH密钥**

```
ssh-keygen -t rsa -C "your_email@youremail.com"  #使用你提供的邮件地址创建一个新的SSH密钥
```

​		然后会出现

```
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/xxx/.ssh/id_rsa):
Created directory ‘/Users/xxx/.ssh’.
Enter passphrase (empty for no passphrase):				//这里需要输入密码
Enter same passphrase again:											//再次输入密码
```

​		成功的话终端会出现

```
Your identification has been saved in 后面还有一大串
```

​	**2.将ssh写入github**

​		登录自己的GitHub主页找,点击右上角个人的小图标-Settings->SSH and GPG keys ->New SSH key

​			![截屏2020-08-24 下午10.05.10](/Users/yilk/Desktop/Markdown/配置问题/pic/截屏2020-08-24 下午10.05.10.png)

​		Title 随意 

​		终端输入

```
open .ssh/id_rsa.pub 
```

​		回车后，就会新弹出一个终端，然后复制里面的内容到key中，最后点击图中的绿色按钮即可。

​	**3.链接验证**

```
ssh -T git@github.com 
```

​		终端显示

```
Hi xxxx! You've successfully authenticated, but GitHub does not provide shell access. //这就表明链接成功
```

​	**4.设置uername和email**

​		git会根据用户名和邮箱跟踪是谁做的提交。并且，之后会使用这些信息去关联你的提交和github的账户。

```
git config --global user.name "x x x x x"
git config --global user.email "xxxxx"
```

### 3⃣️提交项目到GitHub

​	**1.在GitHub上创建好一个repository**

​	**2.点击自己刚刚创建好的repository，点击绿色按钮Code->Use ssh->复制框中的链接**

​	**3.在终端切换到自己想要的路径，输入：**

```
git clone 复制的链接
```

​	**4.等待克隆完成**

