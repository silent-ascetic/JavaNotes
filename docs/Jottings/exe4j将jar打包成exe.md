# exe4j将jar打包成exe

#### 启动exe4j

![image-20200510213319005](https://gitee.com/silent-passer/Img/raw/master/img/image-20200510213319005.png)

#### 选择jar打包exe

![image-20200510213443304](https://gitee.com/silent-passer/Img/raw/master/img/image-20200510213443304.png)

#### 设置应用名称和创建位置

**第二个选择的路径最好没中文**

![image-20200510214253328](https://gitee.com/silent-passer/Img/raw/master/img/image-20200510214253328.png)

#### 设置应用信息

![image-20200510215246999](https://gitee.com/silent-passer/Img/raw/master/img/image-20200510215246999.png)

#### 进一步设置

![image-20200510215427584](https://gitee.com/silent-passer/Img/raw/master/img/image-20200510215427584.png)

#### 一直下一步到下图界面

`-Dfile.encoding=utf-8`

![image-20200510215909472](https://gitee.com/silent-passer/Img/raw/master/img/image-20200510215909472.png)

#### 添加jar文件

![image-20200510220045809](https://gitee.com/silent-passer/Img/raw/master/img/image-20200510220045809.png)

#### 设置启动类

![image-20200510220715163](https://gitee.com/silent-passer/Img/raw/master/img/image-20200510220715163.png)

#### 下一步设置jdk版本

![image-20200510221106442](https://gitee.com/silent-passer/Img/raw/master/img/image-20200510221106442.png)

#### 设置jre

**下图中“JAVA_HOME”和“JDK_HOME”必须是jre路径才行。这三项在exe4j 6.02中默认添加**

![image-20200626223849694](https://gitee.com/silent-passer/Img/raw/master/img/image-20200626223849694.png)

**若别人的电脑中没装Java或jdk，在上面填的exe文件的输出文件夹中放置jre，然后添加jre路径。如果上面填的输出文件路径中有中文，那就算添加了jre相对路径程序也检测不到**

**注：**如果输出文件夹含中文，其父目录不含，也可以将jre放在其父目录，或者其不含中文的父目录的父目录（无限套娃）。

![image-20200626225209896](https://gitee.com/silent-passer/Img/raw/master/img/image-20200626225209896.png)

![image-20200626225744817](https://gitee.com/silent-passer/Img/raw/master/img/image-20200626225744817.png)

![image-20200626225859329](https://gitee.com/silent-passer/Img/raw/master/img/image-20200626225859329.png)

#### 最后生成exe可执行文件

![image-20200626230114585](https://gitee.com/silent-passer/Img/raw/master/img/image-20200626230114585.png)

![image-20200626230313728](https://gitee.com/silent-passer/Img/raw/master/img/image-20200626230313728.png)

