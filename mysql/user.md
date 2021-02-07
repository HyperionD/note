## MySQL 用户相关
 
1.创建用户
```
mysql> CREATE USER 'username'@'host' IDENTIFIED BY 'password';
 
mysql> GRANT ALL ON *.* TO 'pig'@'%';
```

2.查看用户及加密方式

```
mysql> use mysql;
mysql> select host,user,pluginfromuser;
```

3.修改用户加密方式
```
mysql> update user set plugin='mysql_native_password' where user='root';
```

