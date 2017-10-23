## Python解释器（Python Interpreter）

### 1. 安装

   只要安装相应平台（Linux、Mac OS X、Windows）的Python解释器，就可以编写程序Python程序了。可在[http://www.python.org/downloads/](http://www.python.org/downloads/) 下载安装。
   
   安装过程中注意选择将Python解释器添加到系统路径变量（**path**）中去。当然也可以安装后手动将Python解释器所在的目录添加到系统路径（path）中。比如：
  在Unix系统上将“/usr/local/bin”添加到系统路径PATH，在Windwos系统上将“C:\python36”添加到系统路径Path。

注：你也可以用第三方按照工具安装Python解释器和各种python库，如[anaconda](https://zhuanlan.zhihu.com/p/25198543)

### 2.（调用Python解释器）运行Python程序：  
     
主要有2种方式：

* 交互式解释器: 只要在命令行输入“python”就进入交互解释执行模式。如：
```
$ python
Python 2.5.2 (r252:60911, Feb 22 2008, 07:57:53) 
[GCC 4.0.1 (Apple Computer, Inc. build 5363)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> 1 + 1
2
>>> print("hello world!")
hello world!
>>> **输入 Control-D（Unix平台）, Control-Z（Windows平台） 退出python解释器**
```
    
* 运行脚本程序：命令行输入“python 脚本文件名”执行脚本文件中的python命令，如“python hello.py”就执行脚本文件"hello.py"中的Python命令。所谓脚本文件，就是以文件扩展名“.py”结尾的文件，其中是一些Python命令和注释。注释不是python命令，仅仅用于说明程序的，在一行前面加上“#”，这一行就是注释而不是命令。脚本文件可以用任何文本编辑器（如window的记事本或Unix的vim/vi文本编辑程序）编写。比如"hello.py"文件中内容如下：
```
 # 这是程序注释，对程序进行一些说明
 # 比如下面的是著名的hello world程序，用于在屏幕上打印（输出）字符：“hello world”
 print("hello world")   # print是python自带的一个函数，用于打印（输出）一些信息，比如这里的字符串
```
写好上面的脚本文件并保存为“hello.py”后，我们在命令行进入这个程序所在的目录，然后输入命令“python hello.py”
```
>>> python hello.py
hello world!
```

**文本编辑工具*： 编辑Python脚本文件推荐使用sublime text 或 Notepad++

许多工具如集成开发环境提供了更方便的编写和执行python程序的方式（不在本教程介绍范围里）。
    
* 集成开发环境：用于编写、运行Python脚本程序的图形用户界面程序如IDLE、PyCharm（[PyCharm安装及使用](http://www.jianshu.com/p/042324342bf4)  
    
* jupyter notebook运行Python解释器：在浏览器中jupyter notebook环境下执行Python命令
