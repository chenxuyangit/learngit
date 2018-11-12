## 分支冲突

question：
我们clone项目之后，在本地仓库进行修改，然后我们再提交到远程仓库，但这个时候别人已经在我们提交之前修改了master分支了。

现在master分支和本地我们提交的分支产生了冲突，Git无法执行“快速合并”，只能试图把各自的修改合并起来，但这种合并就可能会有冲突

```Git
$ git merge feature1
Auto-merging readme.txt
CONFLICT (content): Merge conflict in readme.txt
Automatic merge failed; fix conflicts and then commit the result.
```


必须手动解决冲突后再提交。git status也可以告诉我们冲突的文件

我们也可以直接查看文件内容并将其修改

我们可以直接查看readme.txt的内容：

在提交

```git
$ git add files
$ git commit -m "modify file"
```

最后再将分支删除

git log --graph
可以看到分支合并图
