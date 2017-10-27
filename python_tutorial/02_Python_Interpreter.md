## Python解释器（Python Interpreter）

### 1. 安装

   只要安装相应平台（Linux、Mac OS X、Windows）的Python解释器，就可以编写程序Python程序了。可在[http://www.python.org/downloads/](http://www.python.org/downloads/) 下载安装。
   
   安装过程中注意选择将Python解释器添加到系统路径变量（**path**）中去。当然也可以安装后手动将Python解释器所在的目录添加到系统路径（path）中。比如：
  在Unix系统上将“/usr/local/bin”添加到系统路径PATH，在Windwos系统上将“C:\python36”添加到系统路径Path。
  
  1.1) windows 平台
  
    ![](https://docs.python.org/3/_images/win_installer.png)
    
    在上述的安卓过程中选择“Add Python3.6 to Path”就可以了。
    
    如果忘记勾选上述选项，有2种方法：
    
     1） 卸载，重新安装，在安装过程中勾选上述选项。 
     
     2）手工设置环境变量 (不建议初学者)
        a) 将Python的安装目录(如C:\Python3.6)和脚本目录（如C:\Python3.6\script）加到系统路径变量Path中.
        鼠标右键我的电脑  -> 属性 -> 点击高级系统设置 -> 点击环境变量 -> 点击PATH -> 在最后面加上我们的Python安装路径 -> 点击确定。如图：
        
        ![](http://www.runoob.com/wp-content/uploads/2013/11/201209201707594792.png)
        b) 添加Python 环境变量：PYTHONPATH和PYTHONHOME
        
  1.2） Unix和Mac操作系统都自带了Python，直接使用即可。你也可以在[http://www.python.org/download/ ](http://www.python.org/download/ )下载最新版安装。

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
    
* 运行脚本程序：命令行输入“python 脚本文件名”执行脚本文件中的python命令，如“python hello.py”就执行脚本文件"hello.py"中的Python命令。所谓脚本(script)文件（也称为模块(modules)），就是以文件扩展名“.py”结尾的文件，其中是一些Python命令和注释。注释不是python命令，仅仅用于说明程序的，在一行前面加上“#”，这一行就是注释而不是命令。脚本文件可以用任何文本编辑器（如window的记事本或Unix的vim/vi文本编辑程序）编写。比如"hello.py"文件中内容如下：
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

### 参数传递（Argument Passing）

执行python命令时可以传递给它（解释器）一些参数，如“python hello.py”就给解释器传递了一个脚本文件名“hello.py”。python命令后面的脚本文件名和参数都会被转换成一个字符串列表（a list of strings）并赋值给sys模块的argv变量，python程序就可以通过“import sys”即关键字 “**import**”引入sys模块，以便访问其中的变量argv。字符串列表sys.argv的长度至少是1，如果执行python命令时不带任何脚本文件名和参数，那么sys.argv[0]就是一个空串。如果执行“python hello.py”,则sys.argv[0]的值就是“hello.py”即脚本文件名。


例如，我么修改上面的"hello.py"为：
```
# 在这里import模块 -- sys 是一个标准模块名
import sys

print('Hello there ', sys.argv[1])   # python2 : print 'Hello there', sys.argv[1]
# 命令行参数依次存储在sys.argv[1], sys.argv[2] ...
# sys.argv[0] 是脚本名
```

然后执行它，
```
$ python hello.py Guido
Hello there Guido
$ ./hello.py Alice  ## Unix平台可以不输入python，直接输入脚本文件就能执行
Hello there Alice
```

#### 附录：

**文本编辑工具**： 编辑Python脚本文件推荐使用[sublime text](https://www.sublimetext.com/) 或 [Notepad++](https://notepad-plus-plus.org/).

许多工具如集成开发环境提供了更方便的编写和执行python程序的方式（不在本教程介绍范围里）。
    
* 集成开发环境：用于编写、运行Python脚本程序的图形用户界面程序如IDLE、PyCharm（[PyCharm安装及使用](http://www.jianshu.com/p/042324342bf4)  
    
* jupyter notebook运行Python解释器：在浏览器中jupyter notebook环境下执行Python命令
