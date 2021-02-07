# git远程仓库

1. 查看远程仓库信息

```

git remote -v

```

2. 添加远程仓库

```

git remote add origin http://192.168.1.186:9090/git/test.git

```

3. 推送本地项目

```

# 第一次推送时加上-u参数 会把本地分支与远程分支关联起来，后续推送不需要在使用-u参数

 

git push -u origin master

```
