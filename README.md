# PSV-unity-for-me
psv-unity自用工具集合

## 仓库说明

- 此仓库收录@初代npc大大群里面的大佬分享的移植心得

## 移植经验

- vitasdk自制开发崩溃日志查看网址（用于查看.psp2dmp日志文件）：https://github.com/xyzz/vita-parse-core

- psv自制开发静态库编译连接查找：https://gl33ntwine.com/notes/vita-find-symbol.html

- PSVita 移植 Unity 的网络方面的踩坑记录，需要自取：http://note.axibug.com/blog/post/akiragatsu/PSV_Unity_Net_

- UnityUI高版本降级工具（从项目文件从高版本降级到PSVita支持的unity2018版本）：https://github.com/ZUXTUO/UnityUICompatibilityTool

- 编码查询码地址:https://r12a.github.io/app-encodings/

- Unity 中Texture2D高性能像素填充探究：http://note.axibug.com/blog/post/akiragatsu/201f0588de63

- ps vitaSdk-vscode调试插件：https://github.com/DaveeFTW/kvdb

- psv unity调试插件：https://github.com/Ibrahim778/VitaFTPI-Core

  说明：这只允许您读取在 unity 内部 vita 中运行的应用程序中调用的 Debug.Log，就像在 PC 上一样。

  为此，您需要在vita上设置PrincessLog，这是由@The-Princess-of-Sleeping制作的工具。

  您可以从这里下载文件，在taihen配置中安装内核下的skprx，然后安装vpk并输入PC的IP，将端口保留为默认值，然后按保存配置，然后重新启动您的vita。请注意，当您按"开始调试"时，将打开一个新窗口。这是正常的，您可以忽略它，但不要关闭它。
  然后，要从 unity 内部调用日志，您需要将插件文件夹从发布复制到您的资产文件夹中。

  然后，您可以使用提供的示例日志脚本并将其复制到项目中，也可以创建自己的脚本。

  如果使用示例脚本，它将根据平台自动覆盖 debug.logs，因此无需担心。

请记住，这使用官方sdk将其打印到日志中。

因此，请记住在编译最终版本时删除插件和调试脚本。

## 一些有趣的项目

- unity里的x86虚拟机
  
https://github.com/ZUXTUO/Unity3D-based_X86_VirtualMachine

https://github.com/douglasbarnes/vmcs/tree/master

https://github.com/jfd16/Mariana

as3代码解释器c#版

## 发布文件说明：
<img width="636" height="205" alt="image" src="https://github.com/user-attachments/assets/f287a483-35a6-464e-8fa7-57443e81fc41" />


-此文件包含完整的pc端的sony sdk3.5.7版本，文件里已包含了PSVita的unity2018以及对应的资源包

按照教程请参考文件里自带的安装教程进行安装即可！

大概流程就是：
1.下载unity并安装；

2.下载UnitySetup-Playstation-Vita-Support并安装；（注意要和unity的版本要对应）

3.下载对应的psv SDK并解压到任意位置；（unity5.3以下版本需要3.55的sdk，以上需要3.57的sdk）

4.设置环境变量
SCE_PSP2_SDK_DIR=*SDK解压的路径*
SCE_ROOT_DIR=C:\Program Files (x86)\SCE

5.安装sdk里面的pc端的驱动程序等，有顺序要求

6激活unity2018的PSV开发功能的官方激活码已经过期，所以激活我们默认使用unipacker，

文件里有，管理员权限运行一下打下补丁就可以激活开发功能了

7.最后打包时build Type设置成pc hosted，然后用unityTools.exe对文件夹进行处理;(unityTools.exe -i 打包文件夹路径 -o ./ -f -r -p)

使用vita3k模拟器测试即可!

## 特别感谢：

此仓库的教程分享大部分来自这3位大佬

@皓月云

@Olsc

@初代NPC

在此特别感谢这3位大佬的无私奉献！



