# Blender

安装版本：2.82

2.81的改进之一是使用optix来加速cycles（是blender离线渲染引擎的名字）光线追踪。我们熟知的有windows平台上的dxr管线。而optix使得其他操作系统（如linux）也能使用n卡的光线追踪硬件。至此2.81中cycles支持的渲染方式有cpu、gpu通用计算管线cuda、opencl、optix。

## Building

如何自己编译Blender [Building Blender on Windows]：

https://wiki.blender.org/wiki/Building_Blender/Windows

blender的编译需要两个部分

- 一个部分是由svn来版本控制的预编译lib，在下图为pre-compiled libraries部分，路径和blender文件夹同级，为lib/

- 另外一个部分是由git来版本控制的源码，其中有三种：分为intern、extern和source，这也能从图片左侧的路径看得出
  - intern是blender开发的较为底层的一些源码，路径为blender/intern
  - extern是非blender开发（如物理引擎bullet）的源码，路径为blender/extern
  - source是较为上层的源码，路径为blender/source

![blender_code_layout](blender_code_layout.jpg)