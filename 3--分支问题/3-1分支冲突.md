# 分支branch

##### 1.创建分支
```git
$ git checkout -b branchname
//等同与
$ git branch branchname
$ git checkout branchname
```
创建并切换当前分支 -b表示创建
##### 2.修改文件并提交
修改READMEmd文件内容，然后提交
```git
$ git add README.md
$ git commit -m "Modify Content"
```
##### 3.切换回master分支
```git
$ git checkout master
```
##### 4.合并分支
```git
$ git merge branchname
```
##### 5.删除branchname分支
```git
$ git branch -d branchname
```

##### 查看分支
`$ git branch`
