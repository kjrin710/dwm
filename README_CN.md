# dwm-动态窗口管理器

============================

dwm是X的一个非常快速、小型和动态的窗口管理器。

这是我的自定义dwm，从sr/dwm分叉。

要求

------------

为了构建dwm，您需要Xlib头文件。

安装

------------

编辑config.mk以匹配您的本地设置（dwm已安装到

默认情况下为/usr/local命名空间）。

然后输入以下命令来构建和安装dwm（如果必需作为根）：


进行干净安装

运行dwm

-----------

在.xinitrc中添加以下行，以使用startx启动dwm：

exec dwm

要将dwm连接到特定显示器，请确保

DISPLAY环境变量设置正确，例如：

DISPLAY=foo.bar:1 exec dwm

（这将在主机foo.bar的display:1上启动dwm。）

为了在栏中显示状态信息，你可以做一些事情

像这样出现在你的.xinitrc中：

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm

完成

-------------

dwm的配置是通过创建一个自定义config.h来完成的

以及（重新）编译源代码。
