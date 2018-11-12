# 本地仓库操作

### 1.快速创建版本库并且链接远程仓库
一、创建本地版本库
```Git
$ git init
```
二、将文件添加到本地仓库
```Git
$ git add readme.md
$ git add .
```
三、将文件提交到仓库   **-m** 后面接 描述
```Git
$ git commit -m "describe"
```
**注意：在commit 之后文件就会提交到本地仓库，HEAD会指向最近版本**
![](https://cdn.liaoxuefeng.com/cdn/files/attachments/001384907584977fc9d4b96c99f4b5f8e448fbd8589d0b2000/0)

四、在GitHub上右上角找到“Create a new repo”按钮创建项目

关联起来 这后面的添加的是你自己github上项目的网址
```Git
$ git remote add origin https://github.com/chenxuyangit/learngit.git
```

五、添加到远程库

```Git
$ git push -u origin master
```
-u 将本地master分支内容推送到远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。

----------------------
##### Other其他的方法
```Git
$ git status
```
查看当前状态

```Git
$ git diff <filename>
$ git diff HEAD -- <filename>
```
查看修改内容

查看工作区和版本库里面最新版本的区别(**HEAD表示最新版本**)

```Git
$ git clone gitURL
```
克隆远程库
### 2.查看历史

##### 2.1查看历史版本
```Git
$ git log
$ git log --pretty=oneline
```
查看详细历史记录：会显示每一次你commit提交的记录

查看历史简介：--pretty=oneline 后面输入这样的命令可以使其看起来舒服一些

###### 查看历史命令
```Git
$ git reflog
```
记录你的每一次命令

### 3.版本操作
###### 3.1.版本回退
```Git
$ git reset --hard HEAD^
$ git reset --hard <commendId>
```
回退到上一个版本**(HEAD^表示上个版本HEAD^^上上个版本)**

--hard表示将HEAD指针指向 commendId上
![](https://cdn.liaoxuefeng.com/cdn/files/attachments/001384907584977fc9d4b96c99f4b5f8e448fbd8589d0b2000/0)
![](https://cdn.liaoxuefeng.com/cdn/files/attachments/001384907594057a873c79f14184b45a1a66b1509f90b7a000/0)

###### 3.2.撤销修改
```Git
$ git checkout -- file

$ git reset HEAD <file>
```
把file文件在工作区的修改全部撤销（回到上一次git commit或 git add的状态）

用到撤销修改的情况
1. 在工作区乱涂乱画，直接丢弃工作区的修改
2. 乱搞乱搞后还add了添加到了缓存区 那么先用**reset** 回退版本在执行第一步操作 **HEAD表示上个版本**

###### 3.3.删除文件

```git
$ rm files
$ git rm files
$ git commit -m "remove files"
```
删除文件还需要在版本库中删除文件 并且要用commit 提交
