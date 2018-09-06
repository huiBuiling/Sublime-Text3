### Sublime-Text3

##### SublimeText3常用插件及快捷键总结

> 插件操作

```
* Ctrl+Shift+P调出命令面板

* 首先安装package control组件：
    1. ctr+`调出console面板（view --> show console），黏贴运行
    2. import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
    3. 重启Sublime Text 3，在Perferences->package settings中看到package control这一项，则安装成功
    
* 安装插件：Install Package，选择要安装的插件
* 删除插件：Remove Package，选择要删除的插件
* 更新插件：upgrade packages，选择要更新的插件

* error:Install Package后Sublime弹出窗口提示-->'There are no packages available for installation'
出现的原因：可能是IPv6的原因，如果我们的Intent服务提供者（ISP）不支持IPv6就会引发上述错误，
解决方法一：打开C:\Windows\system32\drivers\etc\hosts文件，增加如下对应关系：50.116.34.243 sublime.wbond.net
解决方法二：手动安装插件
    1. 进入sublimetext安装包管理器官网在搜索框里输入你所需要的插件名称
    2. 进入插件的github页面（点击Details下面的github.com）,点击右侧的clone or download -> Download ZIP
    3. 将下载的压缩包解压后放在Preferences->Browse Packages（即packages文件夹）里面，并重命名（去掉文件名中的-master）
    4. 重启Sublimetext3即可安装成功

```

> 常用插件

- [x] Emmet(快速生成html头部信息)

```
1. Ctrl + N，新建一个文档
2. Ctrl + Shift + P，打开命令模式，再输入 sshtml 进行模糊匹配，将语法切换到html模式
3. 输入  !，再按下 Tab键或者 Ctrl + E ，就能快速打开HTML5的整体结构。

快速html头：!(html:5), html:4s, html:4t, html:xxs

快速代码：ul#nav>li.itemS*4>a{Item $}
<ul id="nav">
	<li class="itemS"><a href="">Item 1</a></li>
	<li class="itemS"><a href="">Item 2</a></li>
	<li class="itemS"><a href="">Item 3</a></li>
	<li class="itemS"><a href="">Item 4</a></li>
</ul>

```

- [x] BracketHighlighter(可能需翻墙,用来匹配相对的符号，然后高亮显示，比如{ }、[ ]、" "等符号)

- [x] HTML-CSS-JS Prettify(可能需翻墙)

```
1. 在编辑器的任意一个html/js/css文件中，右击，出现如下图所示，选择Set Plugin Options。或者 ctrl + shift + h ,出现弹窗确认，出现setting窗口
2. cmd: where node 查看本地安装的NodeJS配置环境路径
3. setting窗口
   "node_path":
    {
        "windows": "C:/Program Files/nodejs/node.exe",  //修改为当前 NodeJS配置环境路径 eg: D:/toolUs/nodejs/node.exe
        "linux": "/usr/bin/nodejs",
        "osx": "/usr/local/bin/node"
    }
4. ctrl + shift + h
```

- [x] LESS(支持less语法高亮)
- [x] Less2Css

```
使用说明：ctrl+s保存less文件时，会将目录下所有less文件自动编译为同名的css文件，详细使用方法参见sublime中如何用less实现css预编译
快捷键：ctrl+s
```

- [x] Csscomb(.css 格式化代码)

```
选中css代码，ctrl+shift+c
报错解决：
preference --> package Settigs --> CSSComb --> setting user --> 修改为当前 NodeJS配置环境路径
```

- [x] 格式化代码

```
由于sublime 已经自建了格式化按钮，我们只需为其设置快捷键
preference  ->  Key Bindings -user -->{ "keys": ["ctrl+alt+f"], "command": "reindent" }
```

- [x] SideBarEnhancements（右键菜单增强插件）

```
以 diff 形式显示未保存的修改、在文件管理器中显示该文件、复制文件路径、在侧边栏中定位该文件等功能，
也有基础的诸如新建文件/目录，编辑，打开/运行，显示，
在选择中/上级目录/项目中查找，剪切，复制，粘贴，重命名，删除，刷新等常见功能。
* preferences > package setting > side bar > Key Building-User，
* 键入以下代码，这里设置按Ctrl+Shift+C复制文件路径，按F1~F5分别在firefox，chrome，IE，safari，opera浏览器预览效果
* 注意代码中的浏览器路径要以自己电脑里的文件路径为准。
[
 
    //chrome
    { "keys": ["f1"], "command": "side_bar_files_open_with",
            "args": {
                "paths": [],
                "application": "C:\\Program Files (x86)\\Google\\Chrome\\Application\\chrome.exe",
                "extensions":".*"
            }
     },
    //firefox
    { "keys": ["f2"], "command": "side_bar_files_open_with",
             "args": {
                "paths": [],
                "application": "E:\\软件\\Firefox\\firefox.exe",
                "extensions":".*" //匹配任何文件类型
            }
    },
    //ie
     { "keys": ["f3"], "command": "side_bar_files_open_with",
             "args": {
                "paths": [],
                "application": "C:\\Program Files\\Internet Explorer\\iexplore.exe",
                "extensions":".*"
            }
    },
    ]
```

- [x] SublimeCodeInte（代码提示、补全插件）

```
支持 JavaScript、Mason、XBL、XUL、RHTML、SCSS、Python、HTML、Ruby、Python3、XML、Sass、XSLT、Django、HTML5、Perl、CSS、Twig、Less、Smarty、Node.js、Tcl、TemplateToolkit 和 PHP 等语言，是 Sublime Text 自带代码提示功能的很好扩展。
```

- [x] 拼写检查

```
Preferences > Settings – User，添加以下代码：
"spell_check": true,
```

- [x] sublimeTmpl（按指定快捷键生成模板）

```
使用说明：按指定快捷键生成模板。
快捷键：
ctrl+alt+h 新建html模板文件
ctrl+alt+j 新建javascript模板文件
ctrl+alt+c 新建css模板文件
ctrl+alt+p 新建php模板文件
ctrl+alt+r 新建ruby模板文件
ctrl+alt+shift+p 新建python模板文件
```

- [x] Terminal （ctrl+shift+T，调出终端直接进入项目所在根目录）
- 
```
cmder：http://cmder.net/（终端工具）下载安装
注册到右键菜单：以管理员身份运行终端，执行：Cmder.exe /REGISTER ALL
记得配置环境变量
{
  // window下终端路径
  "terminal": "D:/tools/cmder/cmder/Cmder.exe",
  //  window下终端参数
  "parameters": ["/START", "%CWD%"]
}
```



------------------------------------------------------

- [x] AutoFileName(文件名自动补全)
- [x] ConvertToUTF8(自动转为UTF-8编码类型)
- [x] DeleteBlankLines

```
使用说明：选中需要批量删除空行的部分，Ctrl + Alt + Backspace，选中部分的所有空行就都被删除了
快捷键：ctrl+alt+backspace
```
- [x] DocBlockr(生成js ,php 等语言函数注释,只需要在函数上面输入/** ,然后按tab 就会自动生成注释)
- [x] jQuery(jquery提示)

- [x] @x1. Alignment

```
使用说明：Alignment是一个代码格式化插件，它可以使多行代码中的等号对齐，也可以调整多行代码为一个缩进级别。
快捷键：ctrl+shift+alt+a
```

- [x] SublimeLinter（它可以帮你找出错误或编写不规范的代码 需要安装nodejs,jshint）
- [x] SublimeLinter-jshint（对错误的javascript代码在状态栏进行提示）
- [x] MarkdownEditing（支持Markdown语法高亮显示）
- [x] OmniMarkupPreviewer（用来在浏览器中预览markdown 编辑的效果 快捷键：ctrl+alt+o）

- [x] View In Browser

```
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
```


- [x] ColorPicker 

```
使用说明：获取颜色，即打开调色板 快捷键都是ctrl+shift+c
但是有时会和ConvertToUTF8冲突
打开Sublime Text --> Preferences --> Browse Packages，找到其中想要修改快捷键的文件夹并进入，找到对应操作系统的Default.sublime-keymap文件，修改快捷键
```


- [x] Can I Use（直接调整到caniuse看到当前属性的浏览器支持情况）

- [x] babel

```
使用说明：支持ES6， React.js, jsx代码高亮，对 JavaScript, jQuery 也有很好的扩展。
设置：
打开.js, .jsx 后缀的文件
打开菜单view->Syntax -> Open all with current extension as... -> Babel -> JavaScript (Babel)，选择babel为默认 javascript 打开syntax
```

- [x] Compact​Expand​Css

```
下载地址:https://github.com/TooBug/CompactExpandCss
使用说明：css横竖向排列切换
快捷键：
ctrl+alt[横向排列
ctrl+alt]竖向排列
```



> Sublime Text 3 快捷键大全

- [x] 选择类

```
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
```


- [x] 编辑类


```
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
```

- [x] 搜索类


```
Ctrl+F 打开底部搜索框，查找关键字。

Ctrl+shift+F 在文件夹内查找

Ctrl+P 打开搜索框。举个栗子：1、输入当前项目中的文件名，快速搜索文件，2、输入@和关键字，查找文件中函数名，3、输入：和数字，跳转到文件中该行代码，4、输入#和关键字，查找变量名。

Ctrl+G 打开搜索框，自动带：，输入数字跳转到该行代码。

Ctrl+R 打开搜索框，自动带@，输入关键字，查找文件中的函数名。举个栗子：在函数较多的页面快速查找某个函数。

Ctrl+： 打开搜索框，自动带#，输入关键字，查找文件中的变量名、属性名等。

Ctrl+Shift+P 打开命令框。

Esc 退出光标多行选择，退出搜索框，命令框等。
```


- [x] 显示类


```
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
```
