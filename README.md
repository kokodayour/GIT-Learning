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


# 4.Git项目搭建和远程库拉取

## 1.创建全新仓库

```git
git init
```

