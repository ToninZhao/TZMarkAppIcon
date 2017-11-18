# TZMarkAppIcon
### 步骤:
#### 如果电脑没有安装*ImageMagick*,在终端执行下面的命令:
```
brew install imagemagick
```
#### 然后在回到项目工程目录,进行如下操作:  
__1.将 shell脚本放在项目的根目录下(与 YourApp.xcodeproj 同一层)__  
__2.YourAppName => TARGETS => YourAppName => Build Phases 点击左上角的'+'的图标,选择 New Run Script Phase__  
在 shell 下面的黑色输入框写上shell的路径:
```
"${SRCROOT}/tzmark_icon.sh"
```
如下图所示:  
![add_run_script](https://github.com/ToninZhao/TZMarkAppIcon/blob/master/step01.png "add_run_script")  
__3.修改 Xcode 默认设置__  
```
YourProjectName => PROJECT => 选中项目 => build setting => Compress Png Files => Debug 的属性由 No 改为 Yes.  
YourProjectName => PROJECT => 选中项目 => build setting => Remove Text Metadata From Png Files => Debug 的属性由 No 改为 Yes. 
```
#### 最后,重新 build 项目.  
![](https://github.com/ToninZhao/TZMarkAppIcon/blob/master/AppIcon.png)  
![](https://github.com/ToninZhao/TZMarkAppIcon/blob/master/AppIcon_blur.png) 
