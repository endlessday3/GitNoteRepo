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
- 使用sqlite3桌面工具（）


- [参考资料](https://www.cnblogs.com/aresxin/p/9014617.html)
