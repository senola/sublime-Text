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
    ] 

相关安装插件：
SideBarEnhancements、JsFormate,ConvertToUTF8，Zen Coding，jQuery 

参考资料：

	http://blog.csdn.net/a497393102/article/details/10563791    
	http://blog.csdn.net/zm2714/article/details/7989384


