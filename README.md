侧边栏添加文件夹
===========================================================


This package add icons to folders in the sidebar by overloading package Theme - Default/Default.sublime-theme

Icons from Soda Theme > http://buymeasoda.github.com/soda-theme/

![Sublime Text 2 Sidebar folder icons](https://raw.githubusercontent.com/senola/pictures/master/sublime%20Text/add_folder_black_color.jpg)


![Sublime Text 2 Sidebar folder icons](https://raw.githubusercontent.com/senola/pictures/master/sublime%20Text/add_folder_white_color.jpg)

Screnshot: Sublime Text 2 build 2217 - Win7


配置方法
-----------------------------------------------------------
- Download the zip.
- Close Sublime Text 2
- Extract the folder to Sublime Text 2 <code>/Packages/</code> folder
- Rename <code>/sidebar-folder-icons-for-sublime-text-master/</code> to <code>/Theme - Sidebar Folder Icons/</code>
- Start Sublime Text 2
- Voilà!


其他设置：

#### 1. 界面样式
Preferences -> Settings-User

	 {
		"bold_folder_labels": true, //左侧文件夹字体加粗
		"create_window_at_startup": false, //启动ST时 不自动创建空文件
		"font_face": "Consolas bold", // 字体设置 加粗
		"font_size": 12,
		"highlight_line": true, //光标所处的整行高亮显示
		"highlight_modified_tabs": true, // 修改过未保存的文件标签高亮显示
		"save_on_focus_lost": true, //文件焦点，即切换到另一个文件时自动保存上一个文件内容
        "update_check":false //禁止自动更新
	}
 

#### 2.热键修改

Preference -> Key Bindings-Users

    [
	     // ctrl + D 默认删除一行
	     { "keys": ["ctrl+d"], "command": "run_macro_file", "args": {"file": "Packages/Default/Delete Line.sublime-macro"} },
	     // 整行下移
	     { "keys": ["alt+up"], "command": "swap_line_up" },
	     // 整行上移
	     { "keys": ["alt+down"], "command": "swap_line_down" },
	     // 复制光标整行，并插入在该行之前
	     { "keys": ["ctrl+alt+down"], "command": "duplicate_line" },
         // ctrl + L  切换到某一行
         { "keys": ["ctrl+l"], "command": "show_overlay", "args": {"overlay": "goto", "text": ":"} }
         // ctrl + / 自动提示
	 { "keys": ["alt+/"], "command": "auto_complete" },
	 { "keys": ["alt+/"], "command": "replace_completion_with_auto_complete", "context":
		[
			{ "key": "last_command", "operator": "equal", "operand": "insert_best_completion" },
			{ "key": "auto_complete_visible", "operator": "equal", "operand": false },
			{ "key": "setting.tab_completion", "operator": "equal", "operand": true }
		]
	 }
    ] 

相关安装插件：
SideBarEnhancements、JsFormate,ConvertToUTF8，Zen Coding，jQuery，AndyJS2（javascript提示）  


参考资料：

	http://blog.csdn.net/a497393102/article/details/10563791    
	http://blog.csdn.net/zm2714/article/details/7989384

#### 3. sublime3 炫酷主题-- Material Theme


![](http://7xi3m0.com1.z0.glb.clouddn.com/sublime/theme/Material_Theme.png)

- 下载`sublime3`
- 安装Package Control：
  
``` 
	import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())

```
- 搜索“Material Theme”并安装

##### 其他设置

1. Preferences -> Settings-User

```
    {
		"ignored_packages":
		[
			"Vintage"
		],
		"theme": "Material-Theme-Darker.sublime-theme",
	    "color_scheme": "Packages/Color Scheme - Default/Monokai.tmTheme",
		"overlay_scroll_bars": "enabled",
		"material_theme_small_tab": true, 
		//"material_theme_disable_fileicons": true,   // Hide siderbar file type icons
	    "line_padding_top": 3,
	    "line_padding_bottom": 3,
	      // On retina Mac
	    "font_options": [ "gray_antialias" ],
	    "always_show_minimap_viewport": true,
	    "bold_folder_labels": true,
	    // Highlight active indent
	    "indent_guide_options": [ "draw_normal", "draw_active" ],
	    "bold_folder_labels": true,
		"create_window_at_startup": false,
		"font_face": "Consolas bold",
		"font_size": 12,
		"highlight_line": true,
		"highlight_modified_tabs": true,
		"ignored_packages":
		[
			"Vintage"
		],
		"save_on_focus_lost": true,
		"tab_size": 4,
		"update_check": false
	
	}
```

2.Preference -> Key Bindings-Users

```
   [
		// ctrl + D 默认删除一行
	     { "keys": ["ctrl+d"], "command": "run_macro_file", "args": {"file": "Packages/Default/Delete Line.sublime-macro"} },
	     // 整行下移
	     { "keys": ["alt+up"], "command": "swap_line_up" },
	     // 整行上移
	     { "keys": ["alt+down"], "command": "swap_line_down" },
	     // 复制光标整行，并插入在该行之前
	     { "keys": ["ctrl+alt+down"], "command": "duplicate_line" },
	     // ctrl + L  切换到某一行
	     { "keys": ["ctrl+l"], "command": "show_overlay", "args": {"overlay": "goto", "text": ":"} },
	     // ctrl + / 自动提示
		 { "keys": ["alt+/"], "command": "auto_complete" },
		 { "keys": ["alt+/"], "command": "replace_completion_with_auto_complete", "context":
		    [
		        { "key": "last_command", "operator": "equal", "operand": "insert_best_completion" },
		        { "key": "auto_complete_visible", "operator": "equal", "operand": false },
		        { "key": "setting.tab_completion", "operator": "equal", "operand": true }
		    ]
		 }
	]
```
