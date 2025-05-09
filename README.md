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

jdk-17.0.14_windows-x64_bin.exe



**%JAVA_HOME%bin**



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



**提示：如果普通用户不行的话，可以通过管理员的身份打开 CMD。**



##### 1.3.4.Maven配置

进入 `apache-maven-3.9.9` 文件夹，进入 `config` 文件夹，点击 `settings.xml` 文件。



**（1）配置 Maven 本地仓库依赖的存储位置：**



进入 `apache-maven-3.9.9` 文件夹下的 `repo` 文件夹，将路径复制下来，然后返回 `settings.xml `文件：



在 `settings.xml` 的第 `56` 行，输入下面内容，本地路径每个人都不同：



<localRepository>D:\SoftWares\apache-maven-3.9.9\repo</localRepository>

**（2）配置阿里云服务器镜像**



由于 Maven 的默认服务器在国外所以下载依赖会很慢，所以我们需要将其改为国内的阿里云服务器，一般使用的是阿里云的镜像。

在 `settings.xml` 的第 `160` 行，我是打了空格所以会多几行，输入下面命令：



<!-- 阿里云镜像 -->
<mirror>
    <id>aliyunmaven</id>
    <mirrorOf>*</mirrorOf>
    <name>阿里云公共仓库</name>
    <url>https://maven.aliyun.com/repository/public</url>
</mirror>

**（3）配置 JDK 版本**



在 Maven 中配置 JDK 版本，可以确保项目在正确的 JDK 环境下进行构建和运行，避免因 JDK 版本不兼容而导致的编译错误或运行时问题。

在 settings.xml 的 第 200 行，要根据自己下载的 JDK 配置，我这里以 JDK 17 和 JDK 8 为例，输入下面命令：

JDK17

```
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









### 3. 数据库



MySQL

Navicat Premium v17.0.4 x64.zipx



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