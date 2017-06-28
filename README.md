# Sublime-Text3
插件总结
转载自：https://github.com/Jesse121/Sublime_Plugins

SublimeText3常用插件及快捷键总结

删除插件，Ctrl+Shift+P调出命令面板，输入remove，调出Remove Package选项并回车，选择要删除的插件即可
更新插件，upgrade packages，

NO.1 下载安装
点击进入sublime官网,根据自己的电脑系统下载相应的版本
将下载的压缩包解压后直接放进你要安装的文件夹，双击sublime_text.exe即可运行

NO.2 插件安装
这是今天的重点，在安装插件之前我们需要安装package control组件

在线安装
按ctr+`调出console面板,粘贴以下代码（或者SUBLIME TEXT 3面板中的代码）到命令行并回车

import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
重启Sublime Text 3。如果在Perferences->package settings中看到package control这一项，则安装成功。

手动安装
如果你的电脑没有外网权限(小编就是这样)，那只能手动安装了
点击Preferences 选择Browse Packages… ，打开其上一级文件夹Data并进入Installed Packages文件夹
将下载的Package Control.sublime-package文件复制进去，再重启Sublime Text
安装方法介绍

在线安装
按下Ctrl+Shift+P调出命令面板，输入install选择Install Package 选项并回车，
再输入你要安装的插件名称(例如sublime tmpl)，然后在列表中选中要安装的插件。
安装成功后一般在Perferences->package settings中可看到
有些插件有可能在列表中搜索不到，你可以选择手动安装
手动安装
进入sublimetext安装包管理器官网在搜索框里输入你所需要的插件名称
进入插件的github页面（点击Details下面的github.com）,点击右侧的clone or download -> Download ZIP,将下载的压缩包解压后放在Preferences->Browse Packages（即packages文件夹）里面，并重命名（去掉文件名中的-master）
重启Sublimetext3即可安装成功
There are no packages available for installation

现实中没有什么事情总是一帆风顺的，特别是计算机程序，时不时就给你来点意外情况。
例如在在线安装步骤中选择Install Package后Sublime弹出窗口提示
There are no packages available for installation
出现的原因：据说是IPv6的原因，如果我们的Intent服务提供者（ISP）不支持IPv6就会引发上述错误，
解决方法一： 打开C:\Windows\system32\drivers\etc\hosts文件，增加如下对应关系：50.116.34.243 sublime.wbond.net
终极解决方法：用手动安装插件

在线安装的插件介绍

1. Alignment
使用说明：Alignment是一个代码格式化插件，它可以使多行代码中的等号对齐，也可以调整多行代码为一个缩进级别。
快捷键：ctrl+shift+alt+a

2. AutoFileName
使用说明：文件名自动补全

3. BracketHighlighter(需翻墙)
使用说明：BracketHighlighter插件是用来匹配相对的符号，然后高亮显示，比如{ }、[ ]、" "等符号的对应高亮显

4. ConvertToUTF8
使用说明：自动转为UTF-8编码类型

5. DeleteBlankLines（安装不成功。。。。。。）
使用说明：选中需要批量删除空行的部分，Ctrl + Alt + Backspace，选中部分的所有空行就都被删除了
快捷键：ctrl+alt+backspace

6. DocBlockr
使用说明：生成js ,php 等语言函数注释,只需要在函数上面输入/** ,然后按tab 就会自动生成注释

7. Emmet
使用说明：它让编写 HTML 代码变得简单。
Emmet用法参见Emmet插件使用方法总结

8.HTML-CSS-JS Prettify(需翻墙)
使用说明：快速格式化html css js
快捷键：ctrl+shift+h

9. jQuery
使用说明：会出现jquery提示

10. LESS
使用说明：支持less语法高亮

11. Less2Css
使用说明：ctrl+s保存less文件时，会将目录下所有less文件自动编译为同名的css文件，详细使用方法参见sublime中如何用less实现css预编译
快捷键：ctrl+s

12. SideBarEnhancements
使用说明：SideBarEnhancements 是一款很实用的右键菜单增强插件，有以 diff 形式显示未保存的修改、在文件管理器中显示该文件、复制文件路径、在侧边栏中定位该文件等功能，也有基础的诸如新建文件/目录，编辑，打开/运行，显示，在选择中/上级目录/项目中查找，剪切，复制，粘贴，重命名，删除，刷新等常见功能。

13. SublimeCodeInte
使用说明：Sublime​Code​Intel 是一个代码提示、补全插件，支持 JavaScript、Mason、XBL、XUL、RHTML、SCSS、Python、HTML、Ruby、Python3、XML、Sass、XSLT、Django、HTML5、Perl、CSS、Twig、Less、Smarty、Node.js、Tcl、TemplateToolkit 和 PHP 等语言，是 Sublime Text 自带代码提示功能的很好扩展。

14. sublime tmpl ---------教需要
使用说明：按指定快捷键生成模板。
快捷键：
ctrl+alt+h 新建html模板文件
ctrl+alt+j 新建javascript模板文件
ctrl+alt+c 新建css模板文件
ctrl+alt+p 新建php模板文件
ctrl+alt+r 新建ruby模板文件
ctrl+alt+shift+p 新建python模板文件

15. SublimeLinter
使用说明：它可以帮你找出错误或编写不规范的代码 需要安装nodejs,jshint

16. SublimeLinter-jshint
使用说明：对错误的javascript代码在状态栏进行提示，

17. Terminal
使用说明：调出终端直接进入项目所在根目录，这个插件与gulp配合很好用
快捷键：ctrl+shift+t

18. View In Browser
使用说明：sublime以本地服务器方式打开网页 为了使用插件，你需要建立一个sublime-project文件，点击Project->Edit Project 粘贴以下代码(这是我的相关配置),并保存到user目录下

{
    "folders":
    [
        {
            "path": "D:\\wamp\\www"    
        }
    ],
    "settings":
    {
        "sublime-view-in-browser":
        {
            "baseUrl": "http://localhost"  
            "basePath": "D:\\wamp\\www",   //本地虚拟主机根目录
        }
    }
}

快捷键：ctrl+alt+v

19. MarkdownEditing
使用说明：它支持Markdown语法高亮显示。

20. OmniMarkupPreviewer
使用说明：用来在浏览器中预览markdown 编辑的效果 快捷键：ctrl+alt+o

21. ColorPicker 
使用说明：获取颜色，即打开调色板 快捷键都是ctrl+shift+c
但是有时会和ConvertToUTF8冲突
打开Sublime Text --> Preferences --> Browse Packages，找到其中想要修改快捷键的文件夹并进入，找到对应操作系统的Default.sublime-keymap文件，修改快捷键

22. Can I Use
使用说明：可以直接调整到caniuse看到当前属性的浏览器支持情况

23.babel-sublime
使用说明：
支持ES6， React.js, jsx代码高亮，对 JavaScript, jQuery 也有很好的扩展。
设置：
打开.js, .jsx 后缀的文件
打开菜单view->Syntax -> Open all with current extension as... -> Babel -> JavaScript (Babel)，选择babel为默认 javascript 打开syntax



手动安装的插件介绍

注意：手动安装的插件不会自动添加到Package Control.sublime-package文件

1. Compact​Expand​Css

下载地址:https://github.com/TooBug/CompactExpandCss
使用说明：css横竖向排列切换
快捷键：
ctrl+alt[横向排列
ctrl+alt]竖向排列

2. Codelf

下载地址：Codelf for Sublime Text 使用说明：变量命名神器Codelf通过搜索在线开源平台的项目源码帮开发者给变量命名 ，有了它再也不用为了命名而绞尽脑汁了 快捷键：鼠标右键，选择Codelf

待定的插件

sublime git

YUI compress

livestyle

GBKEncoding support 中文支持

php_beautifier

php code sniffer

NO.3 Sublime Text 3 快捷键大全

选择类

Ctrl+D 选中光标所占的文本，继续操作则会选中下一个相同的文本。

Alt+F3 选中文本按下快捷键，即可一次性选择全部的相同文本进行同时编辑。

Ctrl+L 选中整行，继续操作则继续选择下一行，效果和 Shift+↓ 效果一样。

Ctrl+Shift+L 先选中多行，再按下快捷键，会在每行行尾插入光标，即可同时编辑这些行。

Ctrl+Shift+M 选择括号内的内容（继续选择父括号）。

Ctrl+M 光标移动至括号内结束或开始的位置。

Ctrl+Enter 在下一行插入新行。举个栗子：即使光标不在行尾，也能快速向下插入一行。

Ctrl+Shift+Enter 在上一行插入新行。

Ctrl+Shift+[ 选中代码，按下快捷键，折叠代码。

Ctrl+Shift+] 选中代码，按下快捷键，展开代码。

Ctrl+K+0 展开所有折叠代码。

Ctrl+← 向左单位性地移动光标，快速移动光标。

Ctrl+→ 向右单位性地移动光标，快速移动光标。

shift+↑ 向上选中多行。

shift+↓ 向下选中多行。

Shift+← 向左选中文本。

Shift+→ 向右选中文本。

Ctrl+Shift+← 向左单位性地选中文本。

Ctrl+Shift+→ 向右单位性地选中文本。

Ctrl+Shift+↑ 将光标所在行和上一行代码互换（将光标所在行插入到上一行之前）。

Ctrl+Shift+↓ 将光标所在行和下一行代码互换（将光标所在行插入到下一行之后）。

Ctrl+Alt+↑ 向上添加多行光标，可同时编辑多行。

Ctrl+Alt+↓ 向下添加多行光标，可同时编辑多行。

编辑类

Ctrl+J 合并选中的多行代码为一行。举个栗子：将多行格式的CSS属性合并为一行。

Ctrl+Shift+D 复制光标所在整行，插入到下一行。

Tab 向右缩进。

Shift+Tab 向左缩进。

Ctrl+K+K 从光标处开始删除代码至行尾。

Ctrl+Shift+K 删除整行。

Ctrl+/ 注释单行。

Ctrl+Shift+/ 注释多行。

Ctrl+K+U 转换大写。

Ctrl+K+L 转换小写。

Ctrl+Z 撤销。

Ctrl+Y 恢复撤销。

Ctrl+U 软撤销，感觉和 Gtrl+Z 一样。

Ctrl+F2 设置书签

Ctrl+T 左右字母互换。

F6 单词检测拼写

搜索类

Ctrl+F 打开底部搜索框，查找关键字。

Ctrl+shift+F 在文件夹内查找

Ctrl+P 打开搜索框。举个栗子：1、输入当前项目中的文件名，快速搜索文件，2、输入@和关键字，查找文件中函数名，3、输入：和数字，跳转到文件中该行代码，4、输入#和关键字，查找变量名。

Ctrl+G 打开搜索框，自动带：，输入数字跳转到该行代码。

Ctrl+R 打开搜索框，自动带@，输入关键字，查找文件中的函数名。举个栗子：在函数较多的页面快速查找某个函数。

Ctrl+： 打开搜索框，自动带#，输入关键字，查找文件中的变量名、属性名等。

Ctrl+Shift+P 打开命令框。

Esc 退出光标多行选择，退出搜索框，命令框等。

显示类

Ctrl+Tab 按文件浏览过的顺序，切换当前窗口的标签页。

Ctrl+PageDown 向左切换当前窗口的标签页。

Ctrl+PageUp 向右切换当前窗口的标签页。

Alt+Shift+1 窗口分屏，恢复默认1屏（非小键盘的数字）

Alt+Shift+2 左右分屏-2列

Alt+Shift+3 左右分屏-3列

Alt+Shift+4 左右分屏-4列

Alt+Shift+5 等分4屏

Alt+Shift+8 垂直分屏-2屏

Alt+Shift+9 垂直分屏-3屏

Ctrl+K+B 开启/关闭侧边栏。

F11：全屏模式

Shift+F11 免打扰模式
Contact GitHub API Training Shop Blog About
© 2017 GitHub, Inc. Terms Privacy Security Status Help
 You signed in with another tab or window. Reload to refresh your session.
