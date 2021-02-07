## 表空间相关

查看表空间物理文件路径
```- - 
SQL> select name from v$datafile;
```

创建表空间
```
SQL> create tablespace JEECGBOOT datafile '/opt/oracle/app/oradata/orcl/jeecgboot.dbf' size 50M autoextend on next 50M maxsize unlimited;
```

## 用户相关

查看所有用户

```
SQL> select username from dba_users;
```

查看当前用户默认表空间

```
SQL> select username,default_tablespace from user_users;
```

创建用户
```
SQL> create user JEECGBOOT identified by JEECGBOOT; 
```

更改用户默认表空间

```
SQL> alter user <username> default tablespace <tablespace_name>;
```

用户授权

```
SQL> grant connect, resource to JEECGBOOT;
```

查看所有用户表、试图

```
SQL> select * from all_tab_comments;
```

查看当前用户表、试图

```
SQL> select * from user_tab_comments;
```

