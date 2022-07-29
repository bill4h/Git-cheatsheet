# Git 命令备忘录 
    
本文中git常见命令，内容来源：[github-git-cheat-sheet](https://training.github.com/downloads/zh_CN/github-git-cheat-sheet/)。

*常记常忘、常忘常记。好记性不如做笔记!!!* 

## 一、目录
|NO.|内容|NO.|内容|
|:-:|-|:-:|-|
|01|[配置工具](#1配置工具)|04|[更改管理](#4更改管理)|
|02|[创建仓库](#2创建仓库)|05|[重做提交](#5重做提交)|
|03|[分支管理](#3分支管理)|06|[同步更新](#6同步更新)|

## 二、Git常见命令

### 1.配置工具

对所有本地仓库的用户信息进行配置。

|命令描述|命令|
|-|-|
|对你的commit操作设置关联的用户名|`git config --global user.name [name]`|
|对你的commit操作设置关联的邮箱地址|`git config --global user.email "[email address]`|
|启用有帮助的彩色命令行输出|`git config --global color.ui auto]`|

### 2.创建仓库

当着手于一个新的仓库时，你只需创建一次。要么在本地创建，然后推送到 GitHub；要么通过 clone 一个现有仓库。

|命令描述|命令|
|-|-|
|创建一个本地仓库|`git init`|
|本地仓库与远程仓库连接起来|`git remote add origin [url]`|
|Clone下载一个已存在的远程仓库，包括所有的文件、分支和提交(commit)|`git clone [url]`|

### 3.分支管理

你做的任何提交都会发生在当前“checked out”到的分支上。使用 git status 查看那是哪个分支。

|命令描述|命令|
|-|-|
|创建一个新分支|`git branch [brach-name]`|
|切换到指定分支并更新工作目录(working directory)|`git switch -c [branch-name]`|
|将指定分支的历史合并到当前分支|`git merge [branch]`|
|删除指定分支|`git branch -d [branch-name]`|

### 4.更改管理

在使用Git管理版本时的常用于查看和更改的命令。

|命令描述|命令|
|-|-|
|列出当前分支的版本历史|`git log`|
|列出文件的版本历史，包括重命名|`git log --follow [file]`|
|展示两个分支之间的内容差异|`git diff [first-branch]...[second-branch]`|
|输出指定commit的元数据和内容变化|`git diff [commit]`|
|将文件进行快照处理用于版本控制|`git add [file]`|
|将文件快照永久地记录在版本历史中|`git commit -m "descriptive message"`|

### 5.重做提交

|命令描述|命令|
|-|-|
|撤销所有 [commit] 后的的提交，在本地保存更改|`git reset [commit]`|
|放弃所有历史，改回指定提交。|`git reset --hard [commit]`|

小心！更改历史可能带来不良后果。

### 6.同步更改

将你本地仓库的现状同步到远程仓库。

|命令描述|命令|
|-|-|
|下载远端跟踪分支的所有历史|`git fetch`|
|将远端跟踪分支合并到当前本地分支|`git merge`|
|将所有本地分支提交上传到 GitHub|`git push`|
|使用来自 GitHub 的对应远端分支的所有新提交更新你当前的本地工作分支。git pull 是 git fetch 和 git merge 的结合|`git pull`|