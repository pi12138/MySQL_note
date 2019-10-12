# mysql 删除操作

##  删除数据表

drop table table_name;



## 删除数据

- 删除一行指定数据
  - delete from table_name where table_head = 'info';
- 删除一个表中所有数据
  - 清除全部数据，不写日志，不可恢复，速度极快
    - truncate table table_name
  - 清除全部数据，写日志，数据可以恢复，速度慢
    - delete from table_name

## 删除数据库

## drop 命令删除数据库

- drop 命令格式：
  - drop database <数据库名>;