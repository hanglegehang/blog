# Java Web开发环境搭建之windows
>JavaWeb的入门级开发环境为IDE+Tomcat+MySQL，IDE的选择上，常见的选择为Eclipse、Myeclipse或IDEA。

[点我下载所需文件](http://pan.baidu.com/s/1sllgPbf)（也可以根据教程自行下载文件）

eclipse-jee-neon-2-win32-x86_64.zip *---Eclipse*

mysql-installer-web-community-5.7.17.0.msi*---Mysql安装器，需联网使用*

jdk-8u111-windows-x64.exe *---JDK*

apache-tomcat-8.5.9-windows-x64.zip *---Tomcat*



## 一、jdk环境配置
#### 1、下载java
到[oracle.com](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)下载java，具体版本根据自己系统下载。
![](http://oj8v2br1f.bkt.clouddn.com/Jietu20170104-153630.jpg)
#### 2、安装jdk
下载得到jdk-8u111-windows-i586.exe，直接双击运行安装，一路next就可以，默认是安装到系统盘下面的Program Files，我这里装在C:\Java下面，注意安装完jdk之后会自动运行安装jre，这时的安装路径最好和jdk一样，方便管理，我的都是在C:\Java下面。
#### 3、配置环境变量
右击“我的电脑”，点击“属性”；选择“高级”选项卡，点击“环境变量”； 在“系统变量”中，设置3项属性，JAVA_HOME,PATH,CLASSPATH(大小写无所谓),若已存在则点击“编辑”，不存在则点击“新建”；一般 PATH都是已经存在的。
<br>
配置如下：
JAVA_HOME：C:\Java\jdk1.8.0_05
Path：%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;  **注意分号**
配置如图
![](http://oj8v2br1f.bkt.clouddn.com/2.png)

![](http://oj8v2br1f.bkt.clouddn.com/3.png)

### 4、测试
然后进入CMD命令测试下自己的Java是否安装成功；测试命令java -version
出现java版本信息的话就证明Java环境已经配置成功了
## 二、Tomcat服务器
>Tomcat常用作servlet的运行容器，在JavaWeb开发中广泛使用，当然，Tomcat也可为提供HTML页面服务。

先到[Tomcat官网](http://tomcat.apache.org)下载Tomcat
![](http://oj8v2br1f.bkt.clouddn.com/4.jpg)
解压下载的apache-tomcat-8.5.9-windows-x64.zip 到任意目录
## 二、Mysql数据库
下载mysql安装器mysql-installer-web-community-5.7.17.0.msi
1、默认
![](http://oj8v2br1f.bkt.clouddn.com/5.png)
2、默认
![](http://oj8v2br1f.bkt.clouddn.com/6.png)
3、设置密码
![](http://oj8v2br1f.bkt.clouddn.com/7.png)
4、点击桌面右下角图标，点击Manager Instance，进入MySql Workbench(管理工具）
![](http://oj8v2br1f.bkt.clouddn.com/8.jpg)
5、输入刚才设置的密码
![](http://oj8v2br1f.bkt.clouddn.com/9.png)
6、mysql管理界面
![](http://oj8v2br1f.bkt.clouddn.com/10.png)

## 二、Eclipse配置（JDK，Tomcat）
### （一）配置jdk
1、找到Windows--Preferences--Java--Installed JREs,点击add
![](http://oj8v2br1f.bkt.clouddn.com/13.png)
2、如图
![](http://oj8v2br1f.bkt.clouddn.com/14.png)
3、点击Directory,选择jdk路径
![](http://oj8v2br1f.bkt.clouddn.com/15.png)
4、配置结果
![](http://oj8v2br1f.bkt.clouddn.com/16.png)
### （二）配置tomcat
1、Windows--Preferences--Server--Runtime Environment
![](http://oj8v2br1f.bkt.clouddn.com/17.png)
2、Browse 选择Tomcat路径，JRE选择jdk
![](http://oj8v2br1f.bkt.clouddn.com/18.png)
### （三）页面测试
1、新建一个Dynamic Web Project，点next
![](http://oj8v2br1f.bkt.clouddn.com/19.png)
2、别忘记点这个
![](http://oj8v2br1f.bkt.clouddn.com/20.png)
3、新建项目的目录
![](http://oj8v2br1f.bkt.clouddn.com/21.png)
4、在WebContent下新建一个Jsp文件
![](http://oj8v2br1f.bkt.clouddn.com/22.png)
5、内容如图
![](http://oj8v2br1f.bkt.clouddn.com/24.png)
6、右键index.jsp，点击run as -->run on server
![](http://oj8v2br1f.bkt.clouddn.com/23.png)
7、如果出现如图结果成功
![](http://oj8v2br1f.bkt.clouddn.com/26.png)






	

