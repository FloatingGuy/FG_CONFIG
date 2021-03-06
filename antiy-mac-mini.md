##工作电脑配置

###共享的配置

* Chrome
* 印象笔记
* QQ音乐
* Xmind


###不能共享配置的工具
1.Sublime Text


> 插件

    * Package Control
    * File Header
    * CTags
    * Markdown Editing
    * Markdown Preview
    * Vintageous
    * Anaconda      代码分析平台，代码规范检查
    * SideBarEnhancements
    * TrailingSpaces   自动删除空格/显示空格

> 全局配置（user）
    /Preferences/Settings-User

``` sublime
{
    "always_show_minimap_viewport": true,
    "draw_minimap_border": true, //# 让 minimap 里的当前位置更显眼点.
    "highlight_line": true, //# ST 里我经常找不到光标在哪儿, 这个开启后可以高亮当前行
    "highlight_modified_tabs": true, //# 修改了而尚未保存的 tab, 会用橘黄色显示
    "color_scheme": "Packages/User/SublimeLinter/Monokai (SL).tmTheme",
    "font_size": 16,
    "ignored_packages":
    [
        "Vintage"
    ],
    "show_encoding": true, //# 显示文件编码
    "show_full_path": true, //# 标题栏上显示完整路径, 有时候不小心开错了文件, 这样能帮你早点发现.
    "show_line_endings": true,
    "open_files_in_new_window": false, //#  在 Finder 里打开文件时, 不会新开窗口了.
    "vintageous_use_ctrl_keys": true, //# 这样 ST 里的 Vim 就支持 Ctrl + v 列选了.
    "vintageous_use_sys_clipboard": true, //# 让 Vim 与系统公用剪切板
    "word_separators": "./\\()\"':,.;<>~!@#$%^&*|+=[]{}`~?" // # 去掉了 "-"
}
```
[Mac OS X 上 Sublime Text 3 的配置][blog1]

> 快捷键配置
> /Preferences/Key Bindingd-User

```
{ "keys": ["super+left"], "command": "prev_view" },
{ "keys": ["super+right"], "command": "next_view" },
{ "keys": ["super+t"], "command": "new_file" },
{ "keys": ["ctrl+alt+d"], "command": "delete_trailing_spaces" },
{ "keys": ["ctrl+alt+o"], "command": "toggle_trailing_spaces"}
```

> File Header模板配置
    /Preferences/Package Settings/File Header/Settings-User

```
{
    "Default": {
        "email": "xxxx@qq.cn",
        "author": "xxxx"
    }
}
```

###管理类
2. Alfred

###工具类
3. Pd
4. wine
5. 迅雷
6. Dash
7. Unclutter
8. synergy Gliffy
9. Digrams
10. Snagit
11. Beyond
12. 010Edit

###阅读类
13. Pocket
14. CHM Reader




##Reference
[blog1]:http://guoqiao.me/post/2015/0110-sublime-text-config-for-mac-os-x

