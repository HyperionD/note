[在线安装](https://opensourcedbms.com/dbms/installing-mysql-5-7-on-centosredhatfedora)

离线安装

1.删除旧的mysql
```
rpm -e --nodeps `rpm -qa | grep mysql`
```

2.本地安装
```
rpm -ivh mysql-community-common-8.0.20-1.el6.x86_64.rpm
rpm -ivh mysql-community-client-plugins-8.0.22-1.el6.x86_64.rpm
rpm -ivh mysql-community-libs-8.0.22-1.el6.x86_64.rpm
rpm -ivh mysql-community-client-8.0.22-1.el6.x86_64.rpm
rpm -ivh mysql-community-server-8.0.22-1.el6.x86_64.rpm
rpm -ivh mysql-community-libs-compat-8.0.22-1.el6.x86_64.rpm

mysqld --initialize
chown -R mysql:mysql /var/lib/mysql
cat /var/log/mysqld.log |grep password
```

3.修改密码
```sql
mysql> alter user 'root'@'localhost' identified by 'password'
```

4.重新初始化root密码
```bash
mysql_secure_installation
```


