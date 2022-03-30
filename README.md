# MacOS 配置安卓测试环境
  Mac os环境配置安卓虚拟机. 
  
  安装：brew adb android-virtualBox等. 
  
## 首先安装brew
Homebrew是一款Mac OS上的软件包管理工具，自己电脑上有的话不需要重复安装
  中国使用切换源的方式安装:
  `/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)"`. 
  
  国外正常按照官网的cmd安装：
  `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`. 
  
## 使用brew安装adb
  使用brew工具安装：
  `brew install --cask android-platform-tools`. 
  
  自然如果是卸载就是用`uninstall`命令. 
  
  查看安装位置：
  `brew info --cask android-sdk`. 
  
## 安装android模拟器和VitualBox
  这里根据个人喜好下载安装安卓模拟器即可，例如夜神模拟器安装后可以默认安装VitualBox. 
  
## python安装uiautomator2
  `pip3 install --upgrade --pre uiautomator2`. 
  
## python安装pillow模块
  `pip3 install pillow`. 
  
## uiautomator测试并初始化安卓模拟器
  `python3 -m uiautomator2 init`. 
  
## 安装weditor
  `pip3 install -U weditor`. 

## adb连接android模拟器
  `cd /Applications/LocalSetup/Nox\ App\ Player.app`. 
  
  `adb connect 127.0.0.1:62001` 显示connected就是ok. 
  
## 解决adb devices报错
  如果报错显示:`adb server version (32) doesn't match this client (41);killing ... `. 
  表示adb 5037端口被占用了. 
  macos: `lsof -i:5037` 查看占用5037进程的pid
  杀进程: `kill -9 <pid num>` 
  
  
  
  
