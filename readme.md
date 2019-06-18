# SDU抢课脚本

## 前言
此脚本能够消除SDU的童鞋抢不到课的难受感觉。

全平台，全自动，让你轻松上到你想要的课（雾）

To非SDU的童鞋：本脚本是基于QH大学开发的在线选课系统运行的。如果你的学校恰好也是QH大学开发的，那么这套系统改一改可能就可以用上了！

（请修改GPost.kt中的$ROOT变量，建议您打开Chrome浏览器分析一下Request和Respond内容）

免责声明：本脚本仅供网络编程学习参考，一切用于违法行为或一切因使用此脚本导致的直接或间接损失，全体代码贡献者不负任何责任。下载/Fork/Clone/使用本代码即表明您已阅读并同意该免责声明。

## 使用方法
您有两种方法可以使用该脚本，一种是到`Release`页面下载jar包运行，另外一种是下载源代码并执行Main.kt文件。

注意，无论哪种方法，都要求您的电脑中**正确安装并配置**了`JDK11`。如果您不知道如何安装`JDK11`，请参考以下安装教程：

- Windows10 [JDK11 JAVA11下载安装与快速配置环境变量教程](https://blog.csdn.net/weixin_40928253/article/details/83590136)
- Mac OSX   [mac系统下安装Java开发环境（一）——JDK安装](https://jingyan.baidu.com/article/7f766daffd99354101e1d095.html) (本篇介绍的是安装JDK1.8，但原理和JDK11的安装差不多)
- Linux     [linux18.04下安装的jdk11.0.2](https://www.cnblogs.com/hhxz/p/10547729.html)

JDK11的下载链接：[Java SE Development Kit 11 Downloads](https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html)

### 下载jar包运行
下载并解压zip文件，您将会得到`SDUClass.jar`文件和config.ini文件。

您可以将这两个文件移动到任何**有执行权限和读写权限**的文件目录中，并且保证两个文件在同一目录下。

使用文字编辑工具（Windows记事本，Mac文本编辑器等）打开config.ini文件，您将会看到：
```
# powered by Grapes
username 账号
password 密码
# 格式：course 课程号 课序号
course SQ0000037H 400
course SQ0000045N 400
```

其中，每行前面带有"#"的是注释行，对程序的运行没有影响。

将`账号`两个字替换为您在选课系统中的用户名，将`密码`替换为密码。

然后您可以看到下面有两行course设置，这些设置只是样例，将它们删除即可。

例如，您要选择的课课程号是SQ0000037H，课序号是400，那么就在ini文件中添加一行`course SQ0000037H 400`。

请确保您的配置是正确的，以免造成意想不到的错误。

如果您是Windows用户：打开CMD，将当前目录修改为jar包和ini文件所在的目录。   
如果您是MacOSX/Linux用户：打开终端（Terminal），通过cd命令将当前目录修改为jar包和ini文件所在的目录。

之后输入`java -jar SDUClass.jar`，即可看到程序正在运行了。

### 直接下载源码
本代码采用`Intellij Idea`编辑器进行编写，上传至GitHub过程中保留了对应的工程描述文件。如果您恰好使用的是`Intellij Idea`编辑器，那么您可以直接通过打开按钮开启工程界面，单击右上角绿色箭头即可运行。

如果您碰巧没有使用该IDE，那么我们推荐您下载一个（雾）。

本代码是Kotlin编写的。

具体运行的话，就是MainKt啦，在此不再赘述。不过在运行以前，还是要配置ini文件，这一点请参照上面**下载jar包运行**章节。

## 版权声明
并没有版权声明。如果有，那就GPL吧，哈哈！

两个大一的小盆友写出来的（确切的说是一个小朋友写，然后另一个小朋友疯狂改。具体的可以看原作者的代码仓库，那个疯狂改的小朋友已经提交了n次Pull Request）

如果您觉得这玩意很好玩，您可以弄下来一起贡献一点代码呀，互相学习一下。

欢迎给我们提供Pull Request呀！