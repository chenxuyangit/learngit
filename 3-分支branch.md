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
```gi
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

```git
$ git merge --no-ff -m "describe"
```
禁止使用Fast forward 模式，Git就会在merge时生成一个新的commit。**使用这种方法合并后的历史有分支能看出曾今合并过。而fast forward合并就看不出来曾经做过合并**
##### 5.删除branchname分支
```git
$ git branch -d branchname
```

##### 查看分支
`$ git branch`
