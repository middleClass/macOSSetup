电脑配置
==============

****
## 目录

*[软件安装](#软件安装)
*[系统配置](#系统配置)
软件安装
------
* Manico
* sourcetree
* homebrew 

系统配置
-----
## 系统配置优化
### 替换Ctrl与Caps Lock按键位置脚本
```
hidutil property --set '{"UserKeyMapping":[{"HIDKeyboardModifierMappingSrc":0x700000039,"HIDKeyboardModifierMappingDst":0x7000000E0},{"HIDKeyboardModifierMappingSrc":0x7000000E0,"HIDKeyboardModifierMappingDst":0x700000039}]}'`
```
### 添加开机任务
上述的替换按键脚本会在重启后失效，我们可以编写自己的shell脚本，并设置为启东市自动执行
首先需要一个配置文件，取名为 ```top.siunim.onlogin.plist```
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
<key>LaunchOnlyOnce</key>
<true/>
<key>Label</key>
<string>com.bestswifter.onlogin</string>
<key>ProgramArguments</key>
<array>
<string>zsh</string>
<string>-c</string>
<string>"$HOME/.macbootstrap/onlogin.sh"</string>
</array>
<key>KeepAlive</key>
<true/>
</dict>
</plist>
```
