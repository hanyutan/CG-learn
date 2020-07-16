## UE4 C++

 预备条件：

- 熟悉C语言语法（指针、函数指针）
- 熟悉C++基本语法（引用、类、面向对象、多态、虚函数）
- 熟悉C++中的模板函数和模板类
- 熟悉C++中的容器



UE4使用的C++11，C++14里的高级用法没有集成进去。

### C语言基础

#### 常用命令

cmd里也能用

- dir 列出当前目录下的文件以及文件夹
- md 创建目录
- rd 删除目录
- cd 进入指定目录
- cd .. 退回到上一级目录
- cd/ 退回到根目录
- del 删除文件
- exit 退出DOS
- cl 编译和链接

#### 如何编译成执行文件

自动关机程序，10min后关机

- `shutdown -s -t 600`关机

- `shutdown -a`取消关机
- `shutdown -r -t`重启

```c
#include <stdlib.h>

void main()
{
    system("shutdown -s -t 600") ;
    //system("shutdown -a") ;
}
```

- 将上述代码保存为`test.c`
- Visual Studio 2015 -> Visual Studio Tools -> VS2015开发人员命令提示
- cd进入代码文件的所在目录，输入`cl test.c`
- 桌面上会出现`test.c`和`test.obj`

#### VS Code+WinGW

参考Link：https://www.zhihu.com/question/30315894

VS Code只是一个纯文本**编辑器**(editor)，不是IDE(集成开发环境)，不含**编译器**(compiler)和许多其它功能，所以编译器要自己装好。

下载编译器MinGW-w64 - for 32 and 64 bit Windows：https://sourceforge.net/projects/mingw-w64/files/
往下稍微翻一下，选最新版本中的`x86_64-posix-seh`
把安装目录`E:\MinGW\bin`加入环境变量
验证是否安装成功：按Win+R，运行cmd，输入gcc，会显示

```shell
gcc: fatal error: no input files
compilation terminated.
```

如果显示“不是内部命令或外部命令”则安装失败

Tips：

- 编译器是把源代码变成可执行文件的，编辑器是你打字的软件。记事本就是一个编辑器，VS Code也是编辑器。**编辑器是无法编译运行程序的**，因为那是编译器的工作
- MinGW是gcc在Windows下的移植，gcc是世界上最流行的C/C++编译器组合。但gcc这个名字也指编译C语言的那个程序，g++才是C++编译器。即gcc程序和g++程序包含在gcc套件以及MinGW里，当只说gcc时要根据语境自己区分
- MinGW只能产生32位程，我们需要使用的是MinGW-w64

#### Visual Studio (Enterprise)

网上找的激活码：https://www.cnblogs.com/known/p/10746861.html

- 菜单栏——文件——新建——项目——C++——空项目
- 右侧解决方案资源管理器——源文件——右键添加新建项——C++文件（如需C文件自行改后缀名为.c）

#### Hello, world!

```c
#include <stdlib.h>
#include <stdio.h>

void main()
{
	printf("Hello, world!");
	getchar();
}
```



















