# 代码管理git/SourceTree
---------------------------
## git是什么，git与svn的区别，各自的优缺点
### git是什么：
> * git是一个免费开源的分布式版本控制系统，分布式相比于集中式的最大区别在于开发者可以提交到本地，每个开发者通过克隆（git clone），在本地机器上拷贝一个完整的Git仓库。
### svn是什么：
> * svn是Subversion的简称，是一个开源的代码版本控制系统，svn管理着随时间改变的数据。这些数据放置在一个中央资料档案库(repository)中。这个档案库很像一个普通的文件服务器,不过它会记住每一次文件的变动。这样你就可以把档案恢复到旧的版本,或是浏览文件的变动历史。
### git和svn的主要区别：
* SVN（Subversion）是集中式管理的版本控制器，而Git是分布式管理的版本控制器。这是两者之间最核心的区别。
### git的优点：
* 分布式，每个参与开发的人的电脑上都有一个完整的仓库，不担心硬盘出问题；
* 在不联网的情况下，照样可以提交到本地仓库，可以查看以往的所有log，等到有网的时候，push到远程即可；
* 非常强大的分支管理功能。
* Git的内容的完整性要优于SVN: Git的内容存储使用的是SHA-1哈希算法。这能确保代码内容的完整性，确保在遇到磁盘故障和网络问题时降低对版本库的破坏。
### git的缺点：
* 学习周期相对而言比较长。
* 不符合常规思维。
* 代码保密性差，一旦开发者把整个库克隆下来就可以完全公开所有代码和版本信息。
### svn的优点：
* 管理方便，逻辑明确，符合一般人思维习惯。
* 较好的权限管理功能，可以精确控制每个目录的权限；
* 使用相对git要简单一点。
* 易于管理，集中式服务器更能保证安全性。
### svn的缺点：
* 集中式，如果中心服务器出现问题，所有人都不能正常干活，恢复也很麻烦，因为SVN记录的是每次改动的差异，不是完整文件；
* 分支功能没有git强大；
* 速度没有git快，如果有五个分支，是把五个分支的文件全部拷下来；
* 必须联网才能commit。
## 为什么要用git
* 方便创建分支，协同工作时能在不影响到其他人的情况下添加或者修改代码。
## git的具体操作，如何提交节点，新建分支，合并分支等（SourceTree）
* 详见[SourceTree基本操作.md](https://github.com/ztywyj/justtest/blob/master/SourceTree%E5%9F%BA%E6%9C%AC%E6%93%8D%E4%BD%9C.md)
## github是什么
> * GitHub是一个面向开源及私有软件项目的托管平台，因为只支持git作为唯一的版本库格式进行托管，故名GitHub。简单来说，GitHub是一个代码托管云服务网站，帮助开发者存储和管理其项目源代码，且能够追踪、记录并控制用户对其代码的修改。
# 开发平台vs2013（.net2.0）
--------------------------------
## vs是什么
> * Microsoft Visual Studio（视觉工作室，简称VS或MSVS）是微软公司的开发工具包系列产品。VS是一个基本完整的开发工具集，它包括了整个软件生命周期中所需要的大部分工具，如UML工具、代码管控工具、集成开发环境（IDE）等等。所写的目标代码适用于微软支持的所有平台，包括Microsoft Windows、Windows Phone、Windows CE、.NET Framework、.NET Compact Framework和Microsoft Silverlight。
## 工作中需要熟悉哪些操作，要掌握哪些操作
# 动态库、静态库的生成与使用（.lib/.dll）
--------------------------------------------------------
## 动态库和静态库的区别，以及各自的优缺点
### 区别：
* 链接时间不同：
静态库的代码是在编译过程中被载入程序中。
动态库的代码是当程序运行到相关函数才调用动态库的相应函数。
* 链接方式不同：
静态库的链接是将整个函数库的所有数据在编译时都整合进了目标代码。
动态库的链接是程序执行到哪个函数链接哪个函数的库。

### 各自的优缺点：
#### 静态库：
* 优点是，在编译后的执行程序不再需要外部的函数库支持，运行速度相对快些；
* 缺点是，如果所使用的静态库发生更新改变，你的程序必须重新编译。
#### 动态库：
* 优点是，动态库的改变并不影响你的程序，所以动态函数库升级比较方便；
* 缺点是，因为函数库并没有整合进程序，所以程序的运行环境必须提供相应的库。

## 动态库/静态库的生成与使用
* 详见[动态库静态库的生成与使用.md](https://github.com/ztywyj/justtest/blob/master/%E5%8A%A8%E6%80%81%E5%BA%93%E9%9D%99%E6%80%81%E5%BA%93%E7%9A%84%E7%94%9F%E6%88%90%E4%B8%8E%E4%BD%BF%E7%94%A8.md)
# vs下的单元测试框架
-------------------------------------
## 白盒测试、黑盒测试
> * 白盒测试又称为结构测试、逻辑驱动测试或基于程序本身的测试，着重于程序的内部结构及算法，通常不关心功能与性能指标。
> * 黑盒测试又被称为功能测试、数据驱动测试或基于规格说明的测试，实际上是站在最终用户的立场上，检验输入输出信息及系统性能指标是否符合规格说明书中有关功能需求及性能需求的规定。
## 测试框架的具体使用
* 详见[vs下的单元测试框架.md](https://github.com/ztywyj/justtest/blob/master/vs%E4%B8%8B%E7%9A%84%E5%8D%95%E5%85%83%E6%B5%8B%E8%AF%95%E6%A1%86%E6%9E%B6.md)
# Markdown
--------------------------------------------
## 为什么要用markdown
* 专注于写作内容，不必为格式困扰，不必多花时间在排版上。
* 简单符号排版，15 分钟上手。
* 纯键盘操作，写作时少调用鼠标，效率能提升很多。
* 使用 Markdown 的 h1、h2、h3 标题，列表、分列表，结构和逻辑都很清晰。排版成同样的效果，md 与 word 比起来简直毫不费力气。另外，还有插入图片、链接、粗体、斜体等功能。
* 纯文本编辑，轻量级。纯文本有很多好处，例如占用空间小、移植方便快捷、可以用 git 比较版本、编辑时不需要软件支持等。
* 目前支持将 md 转换为多种格式，包括 html、tex、pdf 等。
## markdown可以做什么
* 写技术文档、写帮助文档、做记录等。
## markdown常用语法
* 详见[Markdown常用语法.md](https://github.com/ztywyj/justtest/blob/master/Markdown%E5%B8%B8%E7%94%A8%E8%AF%AD%E6%B3%95.md)