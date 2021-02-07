# oracle操作

查看数据库版本信息

```

select * from v$version;

```

确认数据库为CDB模式，仅用于12c以上

```

select name,cdb from v$database;

```

列出pdb

```

SQL> show pdbs;

```

查看CBD容器中包含的PBD容器

```

select con_id,dbid,guid,name,open_mode from v$pdbs;

```

创建新的pdb

```

create pluggable database mypdb admin user admin identified by admin file_name_convert=('/opt/oracle/oradata/ORCL/pdbseed/','/opt/oracle/oradata/ORCL/pdbseed');

```

启动pdb

```

alter pluggable database mypdb open;

```

切换到某个PDB

```

alter session set container=ORCLPDB1

```

切换回CDB容器

```

alter session set container=CDB$ROOT;

```

创建表空间

```

create tablespace <tablespace_name> logging datafile '<filename>' size 32m autoextend on next 32m maxsize unlimited extent management local

```
 
查看所有表空间

```

select name from v$tablespace

```

创建用户，12c需切换到PDB

```

create user <user_name> identified by <password>

grant connect,resource to <user_name>

alter user <user_name> quota unlimited on <tablespace_name>

```

新建同样表结构的表

```

create table new_table as select * from old_table where 1=0;

```
