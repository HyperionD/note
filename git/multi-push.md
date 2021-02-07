

# 推送多个远程仓库

 

编辑 .git/config

 

```

[remote "origin"]

    url = git@github.com:HyperionD/vnote.git

    fetch = +refs/heads/*:refs/remotes/origin/*

    url = git@192.168.1.100:HyperionD/vnote.git   #新增远程仓库

  ```





