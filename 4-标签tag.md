# 标签
<br/>

### 一、创建标签
##### 1.为最新id创建标签
```Git
$ git tag <tagname>
```
默认最新提交的commit上，即HEAD上。当然也可以提交到指定的commit id 上
##### 2.为指定commit id创建标签
通过log找到历史提交的commit id 例：“3a44b21”;
```Git
$ git log --pretty=oneline --abbrev-commit

3a44b21 add a new sentence
dd94ee6 add merge
1777d7f conflict fixed
......

$ git tag <tagname> <commitId>
```
##### 3.为指定commit id创建带有说明的标签

```Git
$ git tag -a <tagname> -m "describe" <commitId>
```

### 二、查看标签
```Git
$ git tag
$ git show <tagname>
```
tag可以查看所有标签名，show 用于查看单个标签信息

### 三、操作标签
##### 1.删除本地标签
```Git
$ git tag -d <tagname>
```
##### 2.标签推送到远程
```Git
$ git push origin <tagname>
$ git push origin --tags
```
**推送指定标签**  |  **推送所有标签**

##### 3.删除远程标签
```Git
$ git tag -d <tagname>
$ git push origin :refs/tags/<tagname>
```
首先要删除**本地**标签，然后在从**远程**删除，删除命令也是push。
