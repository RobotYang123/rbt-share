####**安装方法：**
- <http://docs.phpcomposer.com/00-intro.html#Installation-Windows>（官方中文帮助文档）

----------
####**问题描述 1：**通过`Composer-Setup.exe`安装程序 安装完成后命令无效：
- ![composer命令无效](http://img.blog.csdn.net/20160730203848914)

####**解决办法：**

- 检查系统环境是否自动配置好，若没有请追加Path变量： `C:\ProgramData\ComposerSetup\bin`
- 打开 `cmd` 输入 `composer -v`，显示如下即安装成功，且可全局访问。
	- ![composer安装成功](http://img.blog.csdn.net/20160730204423309)

- 切换到任意目录再次测试一下 `composer -v` ，显示如下安装成功。
	- ![composer安装信息](http://img.blog.csdn.net/20160730204551888)

----------
####**问题描述 2：**通过安装命令手动安装失败：
- ![命令行-版本不行](http://img.blog.csdn.net/20160730204752624)

####**解决办法：**

- 错误提示没有支持 PHP5.5.12 的Composer，更新 `PHP版本5.6` 及以上
- 重新通过命令安装，安装前请先cd到要 `安装目录` （可自行创建指定），例如:
	- `C:\Users\username>cd D:` 切换到D盘
	- `C:\Users\username>cd D:\Composer` 切换到Composer文件夹（自己创建的安装目录）
	- `D:\Composer>php -r "readfile('https://getcomposer.org/installer');" | php` 执行安装命令，从这一步开始及之后和官方文档的教程一样，请自行查阅完成后续操作。

- 安装完成后的文件路径，这时只能在本目录下执行 `composer -v` 命令，即只能局部访问。
	- ![局部访问composer](http://img.blog.csdn.net/20160730205255206)

- 若要全局访问，需要自行配置系统环境变量，追加Path变量 `D:\Composer` (请根据自己的安装目录自行修改)

