# Mac下一些工具的使用

## mac下的netstat

- 参考
[mac下netstat](https://blog.csdn.net/pandafxp/article/details/53748031)

## redis内存分析方法
- redis-cli -> bgsave 生成 dump.rdb 文件
- 拷贝出`/var/lib/redis/dump.rdb`文件
- 使用自己的mac电脑作为数据处理主机
- pip install rdbtools
- rdb -c memory dump.rdb > memory.csv
- 使用sqlite3桌面工具（如`SQLPro for SQLite`）
  + 创建数据库 
  + 建表
    ```sql
    create table memory(database int,type varchar(128),key varchar(128),size_in_bytes int,encoding varchar(128),num_elements int,len_largest_element varchar(128));
    ```
  + 导入csv文件
- `select sum(size_in_bytes)/(1024*1024) from memory;` 查询key总占用内存
- [参考资料](https://www.cnblogs.com/aresxin/p/9014617.html)
