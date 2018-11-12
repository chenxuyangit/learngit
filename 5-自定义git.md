# 自定义Git

### 配置别名

```Git
$ git config --global alias.<newName> <command>

$ git config --global alias.st status
$ git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
```
可以为命令起**别名**，提高开发的速度

### 配置文件

配置Git的时候，加上--global是针对当前用户起作用的，如果不加，那只针对当前的仓库起作用。

配置文件放在.git/config文件中
##### 1.删除自定义git命令
```Git
[alias]
  last = log -1
```
如果想删除自定义命令,在.git的config文件中直接删除即可
