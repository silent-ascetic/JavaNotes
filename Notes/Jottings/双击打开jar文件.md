# 双击打开jar文件

## 修改注册表

#### Windows 7

位置：

`HKEY_CLASSES_ROOT\jar_auto_file\shell\open\command`

修改默认

原数值数据：`"D:\java\jre\bin\javaw.exe" "%1"`

修改后：`"D:\java\jre\bin\javaw.exe" -jar "%1"`

修改好后将jar文件的默认打开程序改为javaw.exe就可以双击运行jar文件了。

#### Windows 10

位置：

`HKEY_CLASSES_ROOT\Applications\javaw.exe\shell\open\command`

修改默认

原数值数据：`"D:\java\jre\bin\javaw.exe" "%1"`

修改后：`"D:\java\jre\bin\javaw.exe" -jar "%1"`

###### ps：javaw.exe文件路径以自己电脑jdk安装路径为准，不要复制粘贴。