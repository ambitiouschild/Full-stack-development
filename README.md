# 全栈环境安装包

#### 介绍
全栈环境安装包Installation-package

#### 软件架构
软件架构说明


#### 安装教程

1.  xxxx
2.  xxxx
3.  xxxx

#### 使用说明

1.  xxxx
2.  xxxx
3.  xxxx

#### 参与贡献

1.  Fork 本仓库
2.  新建 Feat_xxx 分支
3.  提交代码
4.  新建 Pull Request


#### 特技

1.  使用 Readme\_XXX.md 来支持不同的语言，例如 Readme\_en.md, Readme\_zh.md
2.  Gitee 官方博客 [blog.gitee.com](https://blog.gitee.com)
3.  你可以 [https://gitee.com/explore](https://gitee.com/explore) 这个地址来了解 Gitee 上的优秀开源项目
4.  [GVP](https://gitee.com/gvp) 全称是 Gitee 最有价值开源项目，是综合评定出的优秀开源项目
5.  Gitee 官方提供的使用手册 [https://gitee.com/help](https://gitee.com/help)
6.  Gitee 封面人物是一档用来展示 Gitee 会员风采的栏目 [https://gitee.com/gitee-stars/](https://gitee.com/gitee-stars/)

## 全栈



### 1. 后端





















#### 1.1.JDK



##### 1.1.1.下载与安装

1、下载地址
[http](https://so.csdn.net/so/search?q=http&spm=1001.2101.3001.7020)://www.oracle.com/technetwork/java/javase/downloads/index.html

Java archive

2、选择自己想要的版本下载，并且选择自己电脑对应的版本下载

**JDK 1.8 (Java 8)**‌：发布于2014年3月，是长期支持版本（LTS），至今仍被广泛使用。

JDK 1.8与JDK 8是同一版本的不同命名方式（历史遗留问题），而JDK 18是独立的更高版本



3、下载完成之后，双击打开然后点击下一步

4、路径这里个人建议不要放到C盘里去，找个另外的位置存放

5、然后等待加载完成就可以了



##### 1.1.2.配置环境

1、右键点击我的电脑->属性->高级[系统设置]

2.在系统变量下面新增一个变量，名字是JAVA_HOME,代表[JDK安装](https://so.csdn.net/so/search?q=JDK安装&spm=1001.2101.3001.7020)路径

```
JAVA_HOME

D:\SoftWares\Java\jdk-1.8

```



3、添加完成之后选择确认

4、新增加一个CLASSPATH变量属性，继续点新增，然后添加如下代码



```
CLASSPATH

.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar
```

5、找到系统变量中的Path变量，双击进入

6、进去点击新建，

7、输入如下一行代码

```
%JAVA_HOME%\bin
```

8、然后点击确定，每一个窗口都需要点击确认，



1.1.3.验证配置是否成功

1、按下window键+R，在运行栏中输入cmd

2、在命令窗口中输入java - version

3、按下回车之后，出现以下样式则说明安装成功



```
C:\Users\Administrator>java -version
java version "1.8.0_441"
Java(TM) SE Runtime Environment (build 1.8.0_441-b07)
Java HotSpot(TM) Client VM (build 25.441-b07, mixed mode, sharing)

```



#### 1.2.Node.js

node-v22.15.0-x64.msi



#### 1.3.Maven



##### 1.3.1.Maven 简介

apache-maven-3.9.9-bin.zip

Maven 是一个基于项目[对象模型](https://so.csdn.net/so/search?q=对象模型&spm=1001.2101.3001.7020)（POM）的项目管理和自动化构建工具。它主要服务于 Java 平台，但也支持其他编程语言。Maven 的核心优势在于其依赖管理和项目构建的自动化，允许开发者通过简单的配置来管理项目的构建、文档生成、报告、依赖、源代码管理、发布和分发等步骤。



##### 1.3.2.下载 Maven

进入 [Maven 官方网站](https://maven.apache.org/)，找到自己电脑对应系统的 Maven 压缩包版本下载即可，以 Windows 系统为例：

**将下载好的 Maven 压缩包解压，得到下面文件夹：**

**进入文件夹，创建 repo 文件夹，用于存放 Maven 本地仓库依赖，将路径复制下来：**



##### 1.3.3.配置 Maven



###### 1.3.3.1.配置环境变量

返回桌面，右键 `此电脑` >> `属性` >> `高级系统设置` >> `环境变量`，在系统变量模块下新建一个系统变量，具体如下：

MAVEN_HOME

D:\SoftWares\apache-maven-3.9.9

之后在系统变量模块下找到 `Path` 系统变量，操作如下：

变量值：`%MAVEN_HOME%\bin`，可以点击上移，改变系统环境变量的加载顺序。



**完成后，输入 Win + R 运行 CMD ，输入 `mvn --version`（查看 maven 版本），如下所示表示配置成功：。**



```
C:\Users\Administrator>mvn --version
Apache Maven 3.9.9 (8e8579a9e76f7d015ee5ec7bfcdc97d260186937)
Maven home: D:\SoftWares\apache-maven-3.9.9
Java version: 17.0.14, vendor: Oracle Corporation, runtime: D:\SoftWares\Java\jdk-17
Default locale: zh_CN, platform encoding: GBK
OS name: "windows 10", version: "10.0", arch: "amd64", family: "windows"
```





**提示：如果普通用户不行的话，可以通过管理员的身份打开 CMD。**



##### 1.3.4.Maven配置

进入 `apache-maven-3.9.9` 文件夹，进入 `config` 文件夹，点击 `settings.xml` 文件。

D:\SoftWares\apache-maven-3.9.9\conf\settings.xml

**（1）配置 Maven 本地仓库依赖的存储位置：**



进入 `apache-maven-3.9.9` 文件夹下的 `repo` 文件夹，将路径复制下来，然后返回 `settings.xml `文件：

D:\SoftWares\apache-maven-3.9.9\repo

在 `settings.xml` 的第 `56` 行，输入下面内容，本地路径每个人都不同：

```
 <localRepository>D:\SoftWares\apache-maven-3.9.9\repo</localRepository> 
  
  
  <!-- localRepository
   | The path to the local repository maven will use to store artifacts.
   |
   | Default: ${user.home}/.m2/repository
  <localRepository>/path/to/local/repo</localRepository>
  -->
<localRepository>D:\SoftWares\apache-maven-3.9.9\repo</localRepository>
```

localRepository节点用于配置本地仓库，本地仓库其实起到了一个缓存的作用，它的默认地址是 C:\Users\用户名.m2。
当我们从maven中获取jar包的时候，maven首先会在本地仓库中查找，如果本地仓库有则返回；如果没有则从远程仓库中获取包，并在本地库中保存。
此外，我们在maven项目中运行mvn install，项目将会自动打包并安装到本地仓库中。

**（2）配置阿里云服务器镜像**



由于 Maven 的默认服务器在国外所以下载依赖会很慢，所以我们需要将其改为国内的阿里云服务器，一般使用的是阿里云的镜像。

在 `settings.xml` 的第 `160` 行，我是打了空格所以会多几行，输入下面命令：

```
<!-- 阿里云镜像 -->
<mirror>
    <id>aliyunmaven</id>
    <mirrorOf>*</mirrorOf>
    <name>阿里云公共仓库</name>
    <url>https://maven.aliyun.com/repository/public</url>
</mirror>


```

因为国外的服务器下载jar包很慢所以我们改为阿里云服务器

虽然mirrors可以配置多个子节点，但是它只会使用其中的一个节点，即默认情况下配置多个mirror的情况下，只有第一个生效，只有当前一个mirror无法连接的时候，才会去找后一个；而我们想要的效果是：当a.jar在第一个mirror中不存在的时候，maven会去第二个mirror中查询下载，但是maven不会这样做！五、配置JDK
在settings.xml配置文件中找到profiles节点
添加如下配置



**（3）配置 JDK 版本**



在 Maven 中配置 JDK 版本，可以确保项目在正确的 JDK 环境下进行构建和运行，避免因 JDK 版本不兼容而导致的编译错误或运行时问题。

在 settings.xml 的 第 200 行，要根据自己下载的 JDK 配置，我这里以 JDK 17 和 JDK 1.8 为例，输入下面命令：

JDK17

```


<!-- java版本 -->
<!-- JDK17 -->
<profile>
    <id>jdk-17</id>
    <activation>
        <activeByDefault>true</activeByDefault>
        <jdk>17</jdk>
    </activation>
    
    <properties>
    <maven.compiler.source>17</maven.compiler.source>
    <maven.compiler.target>17</maven.compiler.target>
<maven.compiler.compilerVersion>17</maven.compiler.compilerVersion>
</properties>

</profile>
```

JDK1.8

    <!-- JDK1.8 -->
    <profile>
    	  <id>jdk-1.8</id>
    	  <activation>
    		<activeByDefault>true</activeByDefault>
    		<jdk>1.8</jdk>
    	  </activation>
     
    	  <properties>
    		<maven.compiler.source>1.8</maven.compiler.source>
    		<maven.compiler.target>1.8</maven.compiler.target>
    		<maven.compiler.compilerVersion>1.8</maven.compiler.compilerVersion>
    	  </properties>
    </profile>
**注意：本地路径要看自己的情况配置，JDK 的话更改其版本的数字就可以了。**

**注意：操作完后，记得保存 `settings.xml` 文件。**

**（5）检查是否配置成功**



输入 Win + R 运行 CMD ，输入 `mvn help:system`（打印 Maven 信息），如下所示表示配置成功：

```
[INFO] Scanning for projects...
[INFO]
[INFO] ------------------< org.apache.maven:standalone-pom >-------------------
[INFO] Building Maven Stub Project (No POM) 1
[INFO] --------------------------------[ pom ]---------------------------------
[INFO]
[INFO] --- help:3.5.1:system (default-cli) @ standalone-pom ---
[INFO]
```

首次执行 mvn help:system 命令，Maven相关工具自动帮我们到Maven中央仓库下载缺省的或者Maven中央仓库更新的各种配置文件和类库（jar包)到Maven本地仓库中。
下载完各种文件后， mvn help:system 命令会打印出所有的Java系统属性和环境变量，这些信息对我们日常的编程工作很有帮助。

```
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  19.761 s
[INFO] Finished at: 2025-05-09T15:00:19+08:00
[INFO] ------------------------------------------------------------------------
```

##### 1.3.5. IDEA 配置

打开 IDEA，在欢迎界面，依次点击 **`Customize`** >> **`All settings...`** ：

在左上角的搜索拦中输入 **`Maven`**，找到这个，按照自己的情况配置：



在左上角输入 **`Java Compiler`**，找到这个，按照自己的 JDK 情况配置：





#### 1.4.IntelliJ IDEA

ideaIU-2025.1.1.exe

#### 1.5.VSCode

VSCodeUserSetup-x64-1.99.3.exe





#### 1.6.Apifox

Apifox-windows-latest.zip



## 



### 2. 前端



wechat_devtools_1.06.2504292_win32_x64.exe

#### 2.1.Vue

##### 2.1.1.安装node.js

打开node.jd官网[Node.js 中文网](https://dev.nodejs.cn/)

打开安装包直接next就行

不要勾选Automatically install



安装完成后，检查一下是否安装成功

Windows＋R 输入cmd打开命令行，输入一下命令

```
C:\Users\Administrator>node -v
v22.15.0


```

输出版本号就说明安装成功



##### 2.1.2.创建全局安装和缓存日志

在我们的安装目录下，创建名为node_cache和node_global的两个文件夹。

打开管理员命令窗口（一定要是管理员），执行如下命令，将npm的全局模块目录和缓存目录配置到我们刚才创建的那两个目录。

```
npm config set prefix "D:\SoftWares\nodejs\node_global"
 
npm config set cache  "D:\SoftWares\nodejs\node_cache"
```



##### 2.1.3.配置环境变量

```
环境变量怎么变成一行而不是列表了？


变成这个样子一般都是由于你这个 %SystemRoot%\system32  位置被调整在了不是第一个，

所以解决很简单，只需要找到   %SystemRoot%\system32   并提到第一位

一定要注意，不要多截取了，到 分号 为止
```



在设置中搜索并打开环境变量Path

将用户变量最后一行**C:\Users\你的用户名\AppData\Roaming\npm**  

修改为 你的安装目录D:\SoftWares\nodejs\node_global



系统变量中新增一个变量，如下👇

变量名：NODE_PATH

变量值：D:\SoftWares\nodejs\node_modules



系统变量中的path增加下面二个

%NODE_PATH%\node_modules

%NODE_PATH%\node_global



##### 2.1.4.打开权限控制

右击node.js文件夹点击属性，选中安全-编辑

注意，那四个组或用户名都看一下把权限都打开

完全控制--读取

##### 2.1.5.配置淘宝镜像



管理员身份运行cmd,安装淘宝镜像cnpm

淘宝npm镜像原地址 `https://registry.npm.taobao.org` 在2022年6月30日后已不再可用，因此应使用新地址 `https://registry.npmmirror.com/`

```
npm config set registry https://registry.npmmirror.com/

查看cnpm配置修改是否成功


npm config list

npm -v

cache = "D:\\SoftWares\\nodejs\\node_cache"
prefix = "D:\\SoftWares\\nodejs\\node_global"
registry = "https://registry.npmmirror.com/"

; node bin location = D:\SoftWares\nodejs\node.exe
; node version = v22.15.0
; npm local prefix = C:\Users\Administrator
; npm version = 10.9.2
; cwd = C:\Users\Administrator
; HOME = C:\Users\Administrator
; Run `npm config ls -l` to show all defaults.

```



##### 2.1.6.安装Vue CLI脚手架

安装Vue cli

```
npm install -g @vue/cli
```

检查Vue cli是否安装好，出现版本号则安装成功

```
vue --version 

@vue/cli 5.0.8
```



##### 2.1.7.创建并运行Vue项目

创建一个hello-world项目

```
vue create hello-world

$ cd hello-world-vue2
$ npm run serve
```



用VS Code打开项目

第一次运行

Ctrl＋Shift＋`调出终端，输入

```
npm run serve
```

后面就可以直接运行npm脚本

调出npm脚本

在范围内右键 打开npm脚本

点击运行

打开网站链接



执行成功界面

```
 DONE  Compiled successfully in 2317ms                                                                          17:25:42


  App running at:
  - Local:   http://localhost:8080/
  - Network: http://192.168.29.5:8080/

  Note that the development build is not optimized.
  To create a production build, run npm run build.
```



##### 2.1.8.vuex，vue-router的配置

```
// 仓库管理vuex
 
npm install vuex@3
 
// 路由
 
npm install vue-router@3
 
// 请求和响应
 
npm install axios
```



#### 2.2.微信开发工具



### 3. 数据库



#### 3.1.MySQL

##### 3.1.1.MySQL安装

解决[mysql](https://www.php.cn/zt/15713.html)安装时要求输入“current root password”的问题（[windows](https://www.php.cn/zt/15970.html)系统）

在安装MySQL时，如果系统提示输入“current root password”，说明系统中之前已安装过MySQL。 首次安装不会出现此问题。 如果遇到这个问题，并尝试重新安装MySQL却失败，显示“Could not start the service mysql error:0”，则很可能是因为之前的MySQL未完全卸载。请按以下步骤安全卸载：



1. **控制面板卸载:** 首先，在控制面板中卸载MySQL。
2. **停止MySQL服务:** 按下Ctrl + R，输入services.msc打开服务管理器。 找到并停止所有与MySQL相关的服务。
3. **删除MySQL安装目录:** 删除MySQL的安装目录下的所有文件。这通常包含在C盘和D盘中的多个文件夹。
4. **删除程序数据文件夹:** 删除程序数据文件夹中MySQL的相关文件夹。 在Windows 7或Vista系统中，该文件夹通常隐藏，需要显示隐藏文件才能查看（在文件夹选项中设置）。 在XP系统中，则在“Documents and Settings”文件夹中查找。
5. **删除注册表项:** 打开注册表编辑器（Ctrl + R，输入regedit）。 删除以下注册表项（注意，ControlSet001和ControlSet002的数字可能不同，例如ControlSet005、ControlSet006等，请仔细检查并删除所有相关的项）：
   - HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Services\Eventlog\Application\MySQL
   - HKEY_LOCAL_MACHINE\SYSTEM\ControlSet002\Services\Eventlog\Application\MySQL
   - HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Eventlog\Application\MySQL
6. **删除my.ini文件:** 检查C:\WINDOWS目录下是否存在my.ini文件，如果存在，请将其删除。

完成以上步骤后，您可以重新安装MySQL。



MySQL问题：2002 - Can‘t connect to server on ‘localhost‘(10061)【已解决】

**将mysql加入到Windows的服务中。切换到mysql安装目录下的bin文件夹，命令行运行"mysqld --install"**



cd C:\Program Files\MySQL\MySQL Server 8.0\bin

mysqld --install

Service successfully installed.



net start mysql

MySQL 服务正在启动 .
MySQL 服务无法启动。

服务没有报告任何错误。

请键入 NET HELPMSG 3534 以获得更多的帮助。

##### 3.1.2.解决方法

**打开计算机管理**

打开服务

MySQL80 手动启动



让后重新连接



##### 3.1.3.权限不足

在MySQL中，当你尝试执行授权命令（如`GRANT ALL PRIVILEGES ON *.* TO 'root'@'localhost'`）但收到“权限不足”的错误时，通常是因为当前登录的用户没有足够的权限来执行这类操作。MySQL的权限管理是基于用户的，每个用户只能执行他们被授权的操作。







##### 3.1.4.解决步骤



1.使用具有足够权限的用户登录**：

通常，你需要以`root`用户或者具有`GRANT OPTION`权限的用户登录。如果你不是以`root`用户登录，可以尝试以下步骤：

- 登录到MySQL服务器作为`root`用户。
- C:\Program Files\MySQL\MySQL Server 8.0\bin >>cmd
- mysql -u root -p
- 输入密码后，你将能够执行授权命令。



【MySql】ERROR 1045 (28000): Access denied for user ‘root‘@‘localhost‘ (using password: YES)解决方案



2.**检查当前用户的权限**：

如果你不是以`root`用户登录，可以检查当前用户的权限，看看是否包含`GRANT OPTION`。

SHOW GRANTS;

这将显示当前用户的所有权限。如果输出中没有`GRANT OPTION`，那么你将无法授权其他用户。

mysql>  SELECT user, host FROM mysql.user WHERE user = 'root';



如果 host 列中没有 localhost 或 %，说明 root 用户没有从该 IP 地址登录的权限。

如果需要允许从localhost 登录（如果允许所有机器那么用%），可以执行如下语句添加权限

CREATE USER 'root'@'localhost' IDENTIFIED BY 'your_password';
GRANT ALL PRIVILEGES ON *.* TO 'root'@'localhost' WITH GRANT OPTION;
FLUSH PRIVILEGES;

##### 3.1.5.重置root 密码

如果忘记 root 密码，可以通过以下步骤重置

重置密码的第一步就是跳过MySQL的密码认证过程

（1）停止 MySQL 服务
sudo systemctl stop mysql

net stop mysql

（2）以安全模式启动 MySQL
sudo mysqld_safe --skip-grant-tables &



命令：`vim /etc/my.cnf`(注：windows下修改的是my.ini)



my.ini是MySQL数据库中使用的配置文件，修改这个文件可以达到更新配置的目的。



mysql没有配置文件 my.ini

在 MySQL 中，`my.ini` 文件是用来存储配置信息的文件，类似于 Linux 系统中的 `my.cnf` 文件。如果你发现 MySQL 没有 `my.ini` 文件，这通常是因为你正在使用的是 Windows 操作系统，而在 Windows 中，MySQL 的配置文件通常是 `my.ini`。如果你的 MySQL 安装是基于 Linux 或 macOS，那么配置文件会是 `my.cnf`。

##### 3.1.6.Windows 上的 my.ini 文件

在 Windows 系统中，如果你发现没有 `my.ini` 文件，你可以按照以下步骤来创建或修改它：

1. 查找默认位置**：

   通常，`my.ini` 文件位于 MySQL 的安装目录下，例如 `C:\Program Files\MySQL\MySQL Server X.Y\`（其中 `X.Y` 是你的 MySQL 版本号）。

2. 创建或编辑 my.ini**：

   如果没有找到 `my.ini` 文件，你可以手动创建一个。使用文本编辑器（如 Notepad++ 或 Visual Studio Code）创建一个新的文本文件，并将其保存为 `my.ini`。

   确保将文件保存在正确的目录中，通常是 MySQL 的安装目录或数据目录中。



恢复my.ini第五步：在mysql根目录下新建文件，文件名命名为my.ini



```
# http://dev.mysql.com/doc/refman/5.6/en/server-configuration-defaults.html
[client]
default-character-set = utf8
[mysql]
default-character-set = utf8
[mysqld]
character-set-client-handshake = FALSE
character-set-server = utf8
init_connect='SET NAMES utf8'
# Remove leading # and set to the amount of RAM for the most important data
# cache in MySQL. Start at 70% of total RAM for dedicated server, else 10%.
innodb_buffer_pool_size = 128M
# Remove leading # to turn on a very important data integrity option: logging
# changes to the binary log between backups.
# log_bin
# These are commonly set, remove the # and set as required.
#注意这个地方要和你安装mysql的路径保持一致。
basedir = C:\Program Files\MySQL\MySQL Server 8.0
datadir = C:\Program Files\MySQL\MySQL Server 8.0\data
port = 3306
# server_id = .....
# Remove leading # to set options mainly useful for reporting servers.
# The server defaults are faster for transactions and fast SELECTs.
# Adjust sizes as needed, experiment to find the optimal values.
join_buffer_size = 128M
sort_buffer_size = 16M
read_rnd_buffer_size = 16M 
sql_mode=NO_ENGINE_SUBSTITUTION,STRICT_TRANS_TABLES
skip-grant-tables
```



恢复my.ini第七步：在mysql中生成新的data文件

在mysql的bin目录下输入cmd回车然后输入一下命令行。

```
mysqld --initialize-insecure --user=mysql
```

出现这种报错是你没有把之前的data文件删除。



**恢复my.ini第八步：重新生成mysql服务，同时绑定my.ini配置文件**

输入一下命令。

```
mysqld --install "MySql57" --defaults-file="C:/Program Files/MySQL/MySQL Server 5.7/my.ini"
```

在my.ini中增加skip-grant-tables 参数，如果启动服务后服务又立即停止，则需要增加shared-memory 参数 ，此步骤主要是为了免密登录mysql（PS 此步骤可以直接 在cmd中直接输入：mysqld --console --skip-grant-tables --shared-memory）


（3）登录 MySQL（无需密码）当需要输入密码时，直接按enter键，便可以不用密码登录到数据库当中）
mysql -u root -p

flush privileges;(首先更新权限)



（4）重置 root 密码
USE mysql; UPDATE user SET authentication_string=PASSWORD('new_password') WHERE User='root'; FLUSH PRIVILEGES; EXIT;



ALTER USER ‘root’@‘localhost’ IDENTIFIED BY ‘新密码’;



.使用vim /etc/my.cnf命令把 my.cnf中添加的skip-grant-table删除



5）重启 MySQL 服务
`sudo systemctl restart mysql`



service mysqld restart



mysql -u root -p

root 用户已经允许从任意主机（%）和本地（localhost）登录，但仍然无法远程连接,请参考4、5、6



4、MySQL 配置问题
检查 bind-address 配置
1、MySQL 默认只监听本地地址（127.0.0.1），需要修改配置以允许远程连接。
2、打开 MySQL 配置文件（通常是 /etc/my.cnf 或 /etc/mysql/my.cnf）。
找到 bind-address 配置项，将其改为 0.0.0.0（监听所有网络接口）或服务器的公网 IP 地址
[mysqld] bind-address = 0.0.0.0

 3、保存文件并重启 MySQL 服务

sudo systemctl restart mysql



- 检查 skip-networking 配置
  确保 MySQL 配置文件中没有启用 skip-networking。如果存在该配置项，将其注释或删除
  `# skip-networking`



5、防火墙配置
检查服务器防火墙
确保服务器的防火墙允许 MySQL 端口（默认是 3306）的入站连接。例如
如果使用 ufw（Ubuntu）：
sudo ufw allow 3306/tcp
如果使用 firewalld（CentOS）：
sudo firewall-cmd --zone=public --add-port=3306/tcp --permanent
sudo firewall-cmd --reload
检查云服务器安全组
如果使用云服务器（如 AWS、阿里云等），确保安全组规则允许从远程 IP 地址访问 MySQL 端口（3306）

3.**授予权限**：



如果当前用户有足够的权限（即有`GRANT OPTION`），你可以为其授予其他用户的权限。例如，如果你想要授予用户`someuser`对所有数据库的所有权限，你可以这样做：

GRANT ALL PRIVILEGES ON *.* TO 'someuser'@'localhost' WITH GRANT OPTION;

FLUSH PRIVILEGES;

这里的`WITH GRANT OPTION`允许`someuser`将权限授予其他用户。

如果你不是以root用户登录，再次以root用户登录并尝试上述授权命令。





4**使用root用户重新登录并尝试授权**：





##### 3.1.7.MySQL命令



```
C:\Users\Administrator>mysql --version
mysql  Ver 8.0.19 for Win64 on x86_64 (MySQL Community Server - GPL)

C:\Users\Administrator>mysql -u root -p
Enter password: ***************
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 15
Server version: 8.0.19 MySQL Community Server - GPL


mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| sys                |
| world              |
+--------------------+
6 rows in set (0.00 sec)

```





#### 3.2.Navicat Premium



激活

Navicat Premium v17.0.4 x64.zipx



新建数据库，然后运行SQL文件



#### 3.5.Redis



### 4. Git



Git-2.49.0-64-bit.exe





Pull Request: 我改了你们的代码, 请拉回去看看吧。

PR 的直译是: 拉取请求。即使会使用 PR 的人还是会有疑惑, 原因是拉取的主体理解有误, PR 的意思是: 一个请对方拉取自己的代码的请求。



在团队中我承担了 Committer 的责任, 也就是帮同事们检视代码 (Code Review) 和合入代码, 经常听到有同事在群里喊: “大佬, 帮我合个 PR”, “大佬, 我刚提交了一个 MR, 帮忙合一下, 急着出补丁”。我有点懵了, PR 和 MR 到底哪个才是正确的, 这两个到底有什么区别, 我决定先搞清楚这两个概念再合入他们的代码。



#### 4.1. 什么是 Pull Request?

PR 的全称是 Pull Request, 经常用 Github 的同学对这个肯定很熟悉了。Github 聚集了 4000 万开发者, 过亿的[开源项目](https://so.csdn.net/so/search?q=开源项目&spm=1001.2101.3001.7020), 如果想给别人的开源仓库贡献代码, 通常是先 fork 别人的项目, 然后本地修改完成提交到自己的个人 fork 仓库, 最后提交 PR 等待别人合入你的代码。



![](D:\Coding\Gitee\Installation-package\fork工作流.png)



fork 工作流

我们重点看一下第 6 步, 小明写完代码了想合入到原作者的仓库, 新建了一个"pull request", 拉请求? 这明明是推啊, 小明将自己的修改推到原作者的仓, 感觉叫"push request"比较合适吧。

既然 Github 坚持叫"pull request", 我们试着理解一下它的思路, 小明写完代码了心里肯定是在想: 原作者大神, 我改了点东西, 你快把我的修改拉回去吧。站在原作者的角度思考, 叫 pull request 好像也说得过去, 每天有大量的人从我这里 fork 代码走, 我只会拉取我感兴趣的代码回来。



#### 4.2. 什么是 Merge Request?



MR 的全称是 Merge Request, 相信玩过 [Gitlab](https://so.csdn.net/so/search?q=Gitlab&spm=1001.2101.3001.7020) 的同学都知道这个。

插播一下, Github 这么好用了为什么还有人玩 Gitlab, 这就要几年前说起了。在微软没有收购 Github 之前, Github 上面所有的项目必须是公开的, 也就是说自己很渣的代码也必须要公开, 不能藏着噎着。但是在一些小的公司或者创业团队, 代码这种核心资产是不希望被公开, 他们迫切需要私密仓这种需求, 所以很多人都选择了 Gitlab。当然后面 Github 也放开了私有仓库, 这是后话了。





merge 工作流

团队中每个人都从远程仓库 develop 分支拉取代码, 本地基于 develop 分支新建特性分支, 修改完代码将特性分支推到远程仓, 紧接着新建 Merge Request 期望将自己的特性分支合入 develop 分支。

从上面这个流程来看 Merge Request 就是将自己的特性分支合入到主干分支。



#### 4.3. Pull Request VS Merge Request

- Github 是玩 fork 模式的, 开发者提交自己的代码新建 Pull Request, 请求原作者: “把我的代码拉回去吧”。
- Gitlab 是玩分支模式的, 开发者提交自己的代码新建 Merge Request, 想将自己的特性分支合并到主干。



上面总结的好像很有道理, 但是不要忘了, Github 也可以玩分支模式, Gitlab 也可以玩 fork 模式, 更令人无语的是:

Github 上合并分支还是叫 Pull Request; Gitlab 上 fork 模式也是叫 Merge Request;

不行, 这种答案我没法接受, 去 stackoverflow 上搜一些大家是怎么理解的。果然有一个帖子很火:

Pull request vs Merge request



有一个回答摘取了 Gitlab 的官方解释:



Merge or pull requests are created in a git management application and ask an assigned person to merge two branches. Tools such as GitHub and Bitbucket choose the name pull request since the first manual action would be to pull the feature branch. Tools such as GitLab and Gitorious choose the name merge request since that is the final action that is requested of the assignee. In this article we’ll refer to them as merge requests.



合并或拉取请求是在git管理应用程序中创建的，并要求指定人员合并两个分支。GitHub和Bitbucket等工具选择名称pull请求，因为第一个手动操作将是pull功能分支。GitLab和Gitorious等工具选择名称合并请求，因为这是请求受让人的最终操作。在本文中，我们将把它们称为合并请求。



翻译过来简单理解就是: 这两个没有本质区别, 站在不同立场说法不一样而已。

好了, 官方已经盖棺定论了, 这两个就是一个东西, 不要纠结啦~



从国外到国内都有大量的用户对这个名字不理解, 明明是提交提交代码, 为什么是 pull request, 有些人甚至怀疑是名字打错了。

如果让我来给 Github 取名字, 我可能会取:

- push request 推请求
- merge request 合并请求

想多了, 不会有如果。



#### 4.4总结

Pull Request 和 Merge Request 本质上都是合入代码, 只是站在不同角度有不同的说法而已, 因此在学习和工作中无论用哪一个都没有问题。



#### 4.5. Difference between collaborator and contributor



- `Author`: The person/s or organization that created the project
- `Owner`: The person/s who has administrative ownership over the organization or repository (not always the same as the original author)
- `Maintainers`: Contributors who are responsible for driving the vision and managing the organizational aspects of the project. (They may also be authors or owners of the project.)
- `Contributors`: Everyone who has contributed something back to the project.
- `Community Members`: People who use the project. They might be active in conversations or express their opinion on the project’s direction.
- An outside `collaborator` is a person who isn’t explicitly a member of your organization, but who has Read, Write, or Admin permissions to one or more repositories in your organization.



合作者和贡献者之间的区别

来自GitHub开源指南和GitHub帮助。

- 作者：创建项目的个人或组织
- 所有者：对组织或存储库拥有管理所有权的人（并不总是与原作者相同）
- 维护者：负责推动愿景和管理项目组织方面的贡献者。（他们也可能是项目的作者或所有者。）
- 贡献者：为项目做出贡献的每个人。
- 社区成员：使用该项目的人。他们可能会积极参与对话，或对项目的方向发表意见。
- 外部合作者是指不是您组织的明确成员，但对您组织中的一个或多个存储库具有读取、写入或管理权限的人。



TortoiseGit-preview-2.17.1.0-20250413-c94878f-64bit.msi



#### 4.6.TortoiseGit状态图标不能正常显示的解决办法



1.1. 右键点击桌面空白处，打开[TortoiseGit](https://so.csdn.net/so/search?q=TortoiseGit&spm=1001.2101.3001.7020)的Settings

修改Icon Overlays的Status cachea图标覆盖---windows外壳



重启电脑，你就会发现你的小乌龟箭头出来了。



修复TortoiseGit文件夹和文件图标不显示



按Win+R键打开运行对话框，输入 regedit ，打开注册表；
找到 HKEY_LOCAL_MACHINE\Software\Microsoft\Windows
CurrentVersion\Explorer 新建一个“字符串值”名称为 “Max Cached Icons” 值是 “2000”；
重启一下电脑，看图标是否显示。



#### 4.7.TortoiseGit SSH代理与私钥持久化



SSH 代理与私钥持久化：让你的开发环境不再因重启而中断

在使用 Git、远程服务器或其他依赖 SSH 认证的工具时，私钥是身份验证的核心。然而，很多用户在克隆、推送或拉取代码时，可能遇到如下错误：

```
ssh-keygen -t rsa

按照提示完成三次回车，即可生成 ssh key（如图所示）。生成了了id_rsa和id_rsa.pub

复制选中内容添加到Gitee上 点击个人头像 「设置」->「安全设置」->「SSH公钥」 ，添加生成的 public key 添加到仓库中。（将id_rsa_pub公钥配置到gitee） 

生成known_hosts文件（三个文件缺一不可）
```



-------------------------------------------------------------------------------------------

TortoiseGit提示No supported authentication methods available



`TortoiseGit`远程仓库的公匙无法和本地的密匙进行匹配认证造成的(主要是`TortoiseGit`缺少本地密匙)。由于`TortoiseGit`的默认网络`SSH client`是`TortoiseGitPlink.exe`。因此主要有两种方式来解决该问题：

方法一：

不修改`TortoiseGit`的默认网络`SSH client`，此时需要为`TortoiseGit`添加后缀为`.ppk`的本地密匙。修改`TortoiseGit`的默认网络`SSH client`，使其与`GitBash`的`SSH`相同，即与`GitBash`使用相同的密匙



在应用列表中找到PuTTYgen,点击打开

加载本地.ssh目录下的id_rsa文件

选择后点击确定，同时操作上述第4点，将保存私钥(.ppk)和公钥(复制到.txt文档)



Pageant.exe，添加：gitee.ppk、github.ppk

点击`Add Key`来将本地生成的后缀名为`.ppk`的密匙添加进去

打开TortiseGit的Setting，添加用户名称和邮箱。添加完后，即可通过tortisegit操作了。



方法二：



**修改`TortoiseGit`的默认网络`SSH client`执行程序**

​     由于`TortoiseGit`出现错误，而`GitBash`可以正常使用，所以`GitBash`的`SSH`是正常的。在此将`TortoiseGit`的`SSH client`修改为`GitBash`对应的`SSH`程序。



设置>网络>SSH客户端

最重要的一步找到 ssh.exe，否则的话会报各种各样的错误，有权限不足，有让你输入git账户密码的，因为小乌龟和git有一定冲突默认路径是C:\Program Files\TortoiseGit\bin\sshaskpass.exe需要改成C:\Program Files\Git\usr\bin\ssh.exe



D:\SoftWares\Git\usr\bin\ssh.exe





##### 1. 确认 Git 安装

```
C:\Users\Administrator>git --version
git version 2.49.0.windows.1
```



##### 2. 安装或修复 SSH

如果 Git 已安装但 `ssh` 命令不可用，你可以尝试以下方法：

##### 方法一：重新安装 Git

1. 卸载当前的 Git。
2. 访问 [Git 官网](https://git-scm.com/)下载最新版本的安装程序。
3. 在安装过程中，确保选择了“Use OpenSSH”选项（这通常在“Choosing Components”或“Select Components”步骤中）。
4. 完成安装。

##### 方法二：单独安装 OpenSSH

如果你不想重新安装 Git，可以单独安装 OpenSSH：

1. 访问 [OpenSSH for Windows](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) 的官方文档。
2. 按照文档中的指导安装 OpenSSH。

##### 方法三：检查环境变量

确保 `C:\Program Files\Git\usr\bin\` 目录已经添加到你的系统环境变量中。你可以通过以下步骤检查和添加环境变量：

1. 在 Windows 搜索栏中搜索“环境变量”并选择“编辑系统环境变量”。
2. 在系统属性窗口中，点击“环境变量”按钮。
3. 在“系统变量”区域找到并选择“Path”变量，然后点击“编辑”。
4. 确保 `C:\Program Files\Git\usr\bin\` 已经列在列表中。如果没有，点击“新建”并添加该路径。D:\SoftWares\Git\usr\bin
5. 点击确定保存更改。

### 3. 测试 SSH

##### 重新打开命令行窗口，尝试运行以下命令来测试 SSH 是否可以正常工作：

```bash
ssh -V
```

如果这个命令返回了 SSH 的版本号，那么 SSH 已成功安装并配置。

通过上述步骤，你应该能够解决 `ssh` 命令不可用的问题。如果问题仍然存在，可能需要检查是否有其他系统配置或权限问题影响到了 SSH 的使用。





应用确定一下就可以了，后面就可以使用ssh方式从gitee仓库克隆拉取代码



### 5. 网络



Google Chrome



QQ

UU加速器

百度网盘



夸克网盘

腾讯会议

网易云音乐

微信



cat_verge_x84-setup.exe



QQPCDownload310115.exe



QQPCDownload310115.exe



yuanbao_9017_x64.exe













### 6. 容器



Docker Desktop Installer.exe



MuMuInstaller_3.1.13.0_niesdc-mj22455-baidu-pc-sem-dev_zh-Hans_1734008340.exe





### 8. 业务



office2021_64位W10及系统支持



notepad-setup_9977219414923338632.exe



Typora官网
https://typoraio.cn/
免费使用正版的Typora教程
https://blog.csdn.net/wukongaixuexi/article/details/140735387
Typora激活
https://blog.csdn.net/m0_66987512/article/details/147080134?ops_request_misc=%257B%2522request%255Fid%2522%253A%252209e39978652572284f7e94ae1399c894%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=09e39978652572284f7e94ae1399c894&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-2-147080134-null-null.142^v102^pc_search_result_base8&utm_term=typora%E5%85%B3%E9%97%AD%E6%BF%80%E6%B4%BB%E5%BC%B9%E7%AA%97&spm=1018.2226.3001.4187



### 9.测试



git revert

恢复