# 光驱托盘控制工具
## 程序简介
### 背景
两张图你就懂了  
![光驱](https://storage.deepin.org/thread/202108061919193640_9C40C38A968242FB0183D29A211CA40E.jpg)
![光盘](https://storage.deepin.org/thread/202108061924207351_D70B92325ED1883F36146A72F3C80B56.jpg)
（暴露年龄了）

### 介绍
一款基于 Python3 的 PyQt 制作成的光驱托盘控制软件  
使用 Python3 构建  
（测试平台：deepin 20.2.2）  
截图：  
![主界面（太难截图，截图不到）](https://storage.deepin.org/thread/202108061924578844_截图_选择区域_20210806192325.png)


#### 项目提示  
1、可能弹出光驱时会来回伸缩几遍，这是正常现象  
2、如果出现以下错误  
```bash
qt.qpa.plugin: Could not load the Qt platform plugin "xcb" in "" even though it was found.
This application failed to start because no Qt platform plugin could be initialized. Reinstalling the application may fix this problem.

Available platform plugins are: eglfs, linuxfb, minimal, minimalegl, offscreen, vnc, wayland-egl, wayland, wayland-xcomposite-egl, wayland-xcomposite-glx, webgl, xcb.

已放弃
```
可以输入
```bash
sudo apt install -qq libglu1-mesa-dev libx11-xcb-dev '^libxcb*'
```
否则先输入```export QT_DEBUG_PLUGINS=1```然后把问题和报错信息提 isscue

#### 软件架构  
只要你能运行 python3 以及其需要的库就可以使用  

#### 更新内容：  
无

## 运行  

### 安装  
1、下载 deb 包（例图）  
![发行版](https://storage.deepin.org/thread/202107282058556440_截图_选择区域_20210728205830.png)  
2、安装安装包（例图）  
![sudo dpkg -i](https://storage.deepin.org/thread/202107282101281255_截图_deepin-terminal_20210728210103.png)  
### 使用  
在启动器打开后，会在右下角有一个图标：![右下角小图标](https://storage.deepin.org/thread/20210806192954364_截图_选择区域_20210806192935.png)  
右击即可操作   

### 故障排除
提 isscue 最好，当然有些问题自己无法解决，请大佬 push 一下
如果出现故障，尝试终端运行，如果是可以自行解决的问题，就**自行解决**，如果可以就**提 issues 并提供解决方案**，不行就**提 isscue 并提供程序和终端报错以及程序版本**

#### 已知问题
暂未发现

## 相关项目  
| 项目名称 | 项目地址 |
|   :-:  |      :-:|
| 开关光驱 | https://gitee.com/gfdgd-xi/switch-optical-drive |  