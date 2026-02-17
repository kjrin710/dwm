# dwm - 动态窗口管理器
dwm是一款运行速度极快、体积小巧且功能灵活的 X 系统窗口管理器  
dwm的配置是通过创建一个自定义的 config.h 文件并重新编译源代码来实现的  
这是 [dwm](https://dwm.suckless.org/) 项目的个人分支，该项目源自 [suckless.org](https://suckless.org/)  

## 要求/条件
要构建dwm，你需要Xlib头文件。  

## 安装
修改config.mk文件以适应您的本地环境设置（默认情况下，dwm安装在/usr/local目录中）  
之后，请输入以下命令来构建并安装dwm（如果需要的话，请以root身份执行）：  
`make clean install`  

## 运行 dwm
在您的.xinitrc文件中添加以下内容，即可通过startx命令启动dwm：  
`exec dwm`  

若要将 dwm 连接到指定的显示器，请确保已正确设置了DISPLAY环境变量，例如：  
`DISPLAY=foo.bar:1 exec dwm`  
（这将使 dwm 在主机 foo.bar 的 display :1 上启动）  

## 自定义配置
在原版 dwm 基础上进行了以下个性化调整：  
### 补丁
- actualfullscreen
- hide vacant tags
- pertag
- status2d-systray
### 外观
- **字体**：使用 `fontawesome`，尺寸 16
- **主题**：深蓝色配色
### 快捷键变化
- **修饰键**：默认修饰键ALT（Mod1）替换为Super（MOD4）键
- **新增键位**：
  - 增大/减小amixer音量：`Super + Shift + ↑ / ↓`
  - flameshot全屏截图：`Super + s`
  - Flameshot GUI：`Super + Shift + s`
- **调整键位**：
  - 启动终端：`Super + Shift + Return` -> `Super + Return`
  - zoom：`Super + Return` -> `Super + Shift + Return`
  - 关闭当前窗口：`Super + Shift + c` -> `Super + q`
  - 退出 dwm：`Super + Shift + q` -> `Super + Shift + c`
其他默认快捷键保持不变，具体参考config.h配置文件
