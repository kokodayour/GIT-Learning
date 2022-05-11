# GIT-Learning

*学习一下如何使用GIT*




# 1.Git安装

**Git Bash**: Unix与Linux风格的命令行(推荐)

**Git CMD**: Windows风格的命令行

**Git GUI**: 图形界面的Git, 不建议初学者使用

命令行中

白色: 文件

蓝色: 文件夹

蓝色: 程序




# 2.Linux常用命令

1)cd: 改变目录

2)cd ..: 返回上一级(注意之间的空格)

3)pwd: 显示当前目录路径

4)ls(ll): 列出目录所在内容(更详细)

5)touch: 新建一个文件

6)rm: 删除一个文件

7)mkdir: 新建一个目录

8)rm -r: 删除一个文件夹(切勿使用rm -rf /)

9)mv 移动文件 目标文件: 移动文件夹(保证文件和目标文件夹在同一目录)

10)reset: 重新初始化终端

11)clear: 清屏

12)history: 查看命令历史

13)help: 帮助

14)exit: 退出

15)#表示注释




# 3.Git配置

git config -l 查看Git配置

git config --system --list 查看Git配置

git config --global --list  查看本地Git配置



# 4.Git基本原理

## 四个区域

Git本地有三个工作区域：工作目录（Working Directory）、暂存区(Stage/Index)、资源库(Repository或Git Directory)。如果在加上远程的git仓库(Remote Directory)就可以分为四个工作区域。文件在这四个区域之间的转换关系如下：

![image-20220511105523030](C:\Users\31771\AppData\Roaming\Typora\typora-user-images\image-20220511105523030.png)

- Workspace：工作区，就是你平时存放项目代码的地方
- Index / Stage：暂存区，用于临时存放你的改动，事实上它只是一个文件，保存即将提交到文件列表信息
- Repository：仓库区（或本地仓库），就是安全存放数据的位置，这里面有你提交到所有版本的数据。其中HEAD指向最新放入仓库的版本
- Remote：远程仓库，托管代码的服务器，可以简单的认为是你项目组中的一台电脑用于远程数据交换

## 工作流程

１、在工作目录中添加、修改文件；

２、将需要进行版本管理的文件放入暂存区域；

３、将暂存区域的文件提交到git仓库。

![image-20220511105753664](C:\Users\31771\AppData\Roaming\Typora\typora-user-images\image-20220511105753664.png)




# 5.Git项目搭建和远程库拉取

```git
#本地初始化
git init 
#克隆远程库
git clone git@github.com:hatter-fish/GIT-Learning.git
```



# 6. Git文件操作

- Untracked: 未跟踪, 此文件在文件夹中, 但并没有加入到git库, 不参与版本控制. 通过git add 状态变为Staged.
- Unmodify: 文件已经入库, 未修改, 即版本库中的文件快照内容与文件夹中完全一致. 这种类型的文件有两种去处, 如果它被修改, 而变为Modified. 如果使用git rm移出版本库, 则成为Untracked文件
- Modified: 文件已修改, 仅仅是修改, 并没有进行其他的操作. 这个文件也有两个去处, 通过git add可进入暂存staged状态, 使用git checkout 则丢弃修改过, 返回到unmodify状态, 这个git checkout即从库中取出文件, 覆盖当前修改 !
- Staged: 暂存状态. 执行git commit则将修改同步到库中, 这时库中的文件和本地文件又变为一致, 文件为Unmodify状态. 执行git reset HEAD filename取消暂存, 文件状态为Modified

```bash
# 查看文件状态
git status
# 添加文件至暂存区
git add .
# 提交暂存区代码至本地仓库(带上提交信息)
git command -m [message]
```



# 7. gitignore文件

有些文件是不需要被提交的, 如class文件, node_modules模块

```bash
*.txt        #忽略所有 .txt结尾的文件,这样的话上传就不会被选中！
!lib.txt     #但lib.txt除外
/temp        #仅忽略项目根目录下的TODO文件,不包括其它目录temp
build/       #忽略build/目录下的所有文件
doc/*.txt    #会忽略 doc/notes.txt 但不包括 doc/server/arch.txt
```



# 8. 使用远程库

```bash
# 生成ssh
ssh-keygen -t rsa
```

许可证

![img](https://pic1.zhimg.com/80/v2-6f7178c4e502fc939e371717cd887b6c_1440w.jpg)



# 9. idea集成git

