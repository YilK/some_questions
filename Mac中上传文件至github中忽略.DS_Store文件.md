## Mac中上传文件至github中忽略.DS_Store文件

.DS_Store是Mac OS中 保存文件夹**自定义属性**的隐藏文件，比如：文件的图标位置、视图设置或背景色。



解决办法是在提交之前，每一个repository中新建`.gitignore`文件，并在文件中添加` .DS_Store `

已经提交了的话，进行如下操作：

删除当前目录下的` .DS_Store `

```
find . -name '.DS_Store' -type f -delete
```

最后在提交ok。