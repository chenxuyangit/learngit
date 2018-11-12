# Git

git是分布式版本控制系统（自行百度）

**下面是一张git运行是的工作流程图**
![](https://cdn.liaoxuefeng.com/cdn/files/attachments/001384907702917346729e9afbf4127b6dfbae9207af016000/0)
## 核心概念
### 一、工作区
就是我们在电脑里看到的文件夹，就算是一个工作区 就是上图的左侧
### 二、版本库
在工作区中有一个隐藏的目录名称为.git，是Git的版本库

如果看不见是因为电脑没显示隐藏文件，我的电脑用的是Mac，按下command+shift+。 可以打开

图中 **master** 是git自动生成的第一分支，
stage为**缓存区**

整个个提交文件的流程如下
1. git add …… 将工作区的文件添加缓存区

2. git commit …… 将缓存区的文件提交到 master分支

![](https://cdn.liaoxuefeng.com/cdn/files/attachments/001384907584977fc9d4b96c99f4b5f8e448fbd8589d0b2000/0)
**注意：在commit 提交完成后4321 缓存区将会被清空**
```Git
$ git status
On branch master
nothing to commit, working tree clean
```
