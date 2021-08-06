#! /usr/bin/env python3
########################
# 引入所需库
########################
import os
import sys
import time
import PyQt5.QtWidgets as QtWidgets
import PyQt5.QtGui as QtGui

########################
# 程序所需事件
########################

def Out(self):
    os.system("eject /dev/sr* &")

def In(self):
    os.system("eject /dev/sr* -t &")

def Exit(self):
    sys.exit(0)

def AboutQt(self):
    QtWidgets.QApplication.aboutQt()

def AboutThis(self):
    QtWidgets.QMessageBox.about(None, "关于", "<p align='center'><img src='{}/Icon.png' width='100' height='100'></p><br>{}".format(programPath, aboutProgram))
    

#########################
# 设置程序所需变量
#########################
programPath = os.path.split(os.path.realpath(__file__))[0]
version = "1.0.0"
updateTime = "2021年08月06日"
updateThings = '''无'''
programWebsize = ["https://gitee.com/gfdgd-xi/optical-drive-tray-control", "https://github.com/gfdgd-xi/optical-drive-tray-control"]
aboutProgram = '''一款基于 Python3 的 PyQt 制作成的光驱托盘控制软件<br/>
版本：{}<br/>
更新时间：{}<br/>
更新内容：{}<br/>
程序官网：{}<br/>
©2021-{} gfdgd xi'''.format(version, updateTime, updateThings, str(programWebsize), time.strftime("%Y"))

#########################
# 显示窗口
#########################
app = QtWidgets.QApplication(sys.argv)
icon = QtWidgets.QSystemTrayIcon()
icon.setIcon(QtGui.QIcon("{}/Icon.png".format(programPath)))
icon.setToolTip("光驱控制")
menu = QtWidgets.QMenu()
cdromOut = QtWidgets.QAction(text="弹出光驱托盘", triggered=Out)
cdromIn = QtWidgets.QAction(text="收起光驱托盘", triggered=In)
aboutThis = QtWidgets.QAction(text="关于这个程序", triggered=AboutThis)
aboutQt = QtWidgets.QAction(text="关于 QT", triggered=AboutQt)
exit = QtWidgets.QAction(text="退出", triggered=Exit)
menu.addAction(cdromOut)
menu.addAction(cdromIn)
menu.addSeparator()
menu.addAction(aboutThis)
menu.addAction(aboutQt)
menu.addSeparator()
menu.addAction(exit)
icon.setContextMenu(menu)
icon.show()
sys.exit(app.exec_())
