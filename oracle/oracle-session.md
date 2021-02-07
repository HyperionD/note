

# oracle-session

 

显示系统设置的session数

 

```

SQL> show parameter sessions;

```

 

显示当前session数目

 

```

select count(*) from v$session;

```

 

查看系统资源限制，可以查到processes、session的当前连接数与最大限制数量

 

```

select * from v$resource_limit;

```

 

查看当前所有连接的session

 

```

select * from v$session

```

 

关闭dblink产生的session，必须先执行commit

 

```

alter session close database link <db_link_name>

```

 

删除session

 

```

# sid与serial#通过"select * from v$session"查询

 

alter system kill session 'sid,serial#'

```





