# 代码管理git/SourceTree
* sourcetree是是一个用来管理代码的工具，设置好远程仓库后，可以克隆到本地，在本地进行编辑修改后，先进行暂存、提交，再拉取一下远程仓库看是否有更新或冲突，解决完冲突后可以进行推送，同步到远程仓库。
# 开发平台VS2013（.net2.0）
* vs2013是一个集合了开发程序所需要的各种工具的开发软件，以后用c#编写程序时会用到。
# 动态库/静态库的生成与使用（dll/lib）
* 库就是一个写好的可以复用的代码库，静态库是在链接阶段打包到可执行文件中的，缺点是会浪费内存空间，动态库是在程序运行时才会被载入，避免了空间浪费。
## 静态库的生成
1. 新建一个静态库项目。
2. 在头文件下添加static.h，声明函数。
3. 在源文件下添加static.cpp，将头文件包含进去，写上函数。
4. 在菜单栏生成解决方案，会在工程文件夹Debug目录下看到和项目名称同名的lib文件。

## 静态库的调用
1. 新建项目，将头文件static.h和静态库.lib文件拷贝到项目目录。
2. 在主函数中包含头文件，调用静态库有两种方法，一种是在“属性”，“链接器”，“输入”中的“附加依赖项”里添加lib文件名，还有一种是在代码中添加如
```
#pragma comment(lib, "TestLib.lib")
```
## 动态库的生成
1. 新建项目，应用程序类型选择dll。
2. 在头文件下添加头文件dllgenerator.h，声明函数。
3. 在源文件下添加函数定义文件dllgenerator.cpp，写上函数。
4. 在源文件下添加dllmain.cpp，定义DLL应用程序的入口点。
5. 在源文件下添加模块定义文件Source.def，在文件第一行填入项目名称，在EXPORTS下列出要生成的函数名称。
6. 在菜单栏生成解决方案。
## 动态库的调用
1. 还在看……
# vs下的单元测试框架（测试相关知识点）
1. 新建项目，写入方法，在解决方案里新增另一个单元测试项目，用于测试这个方法。
2. 在单元测试项目中引用这个项目，在单元测试的主程序中写入测试的具体内容和期望的结果。
3. 生成解决方案，之后在“测试”，“窗口”中打开“测试资源管理器”，右击需要进行测试的方法名，运行测试，查看结果。
# markdown（文档书写）
* markdown是一种轻量级标记语言，主要用于书写技术文档，通过简单的标记就可以写出简洁易读的文档。
## 常用的语法
* \# 一级标题 \## 二级标题
* \[链接]\(http://\)
* \!\[图片]\(https://\)
* \> 引用
* \* 无序列表
* 1. 有序列表
* \`\`\`

代码块

\`\`\`
