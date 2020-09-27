## Mac中更改默认的python版本

**问题出现**

在终端中输入 python 出现

```zsh
yilk@yilkdeMacBook-Pro ~ % python

WARNING: Python 2.7 is not recommended. 
This version is included in macOS for compatibility with legacy software. 
Future versions of macOS will not include Python 2.7. 
Instead, it is recommended that you transition to using 'python3' from within Terminal.

Python 2.7.16 (default, Jul  5 2020, 02:24:03) 
[GCC 4.2.1 Compatible Apple LLVM 11.0.3 (clang-1103.0.29.21) (-macos10.15-objc- on darwin
Type "help", "copyright", "credits" or "license" for more information.
```

接着输入 python3 出现

```zsh
yilk@yilkdeMacBook-Pro ~ % python3

Python 3.7.3 (default, Apr 24 2020, 18:51:23) 
[Clang 11.0.3 (clang-1103.0.32.62)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
```



**修改默认的路径**

```zsh
yilk@yilkdeMacBook-Pro ~ % which python
/usr/bin/python
yilk@yilkdeMacBook-Pro ~ % which python3
/usr/bin/python3
yilk@yilkdeMacBook-Pro ~ % alias python="/usr/bin/python3"
```

重点在于找到python3的路径，然后修改默认路径

```
alias python="/usr/bin/python3"
```



再次在终端输入python就可以看到想要的结果了。