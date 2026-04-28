天冷了，电脑电池不行，80%多电量也会突然自动关机，导致记录的log文件（实际是sqlite3的数据库文件）受损无法打开，参考 [修复损坏的 SQLite 数据库文件 (database disk image is malformed)-CSDN 博客] https://blog.csdn.net/hzw2017/article/details/120899945 这个教程修复成功，可以打开，一万多行数据看了下都正常，包含了整个充放电过程。记录在此。
## 关键命令：
### 导出数据到sql文件
```
sqlite>.open xxx
sqlite>.output tmp.sql
sqlite>.dump
sqlite>.quit
```
### 再从sql文件生成新的数据库文件
```
sqlite> .open newDB.db
sqlite>.read tmp.sql
sqlite>.quit
```
成功。

另外今天用到了open modscan做modbus tcp调试，注意地址是十进制还是16进制，今天16进制地址开始没注意，怎么输入也不对，最后才发现软件默认是10进制显示地址的，要切换一下。

![Modbus](https://github.com/AlbertWang2018/blog/assets/36392874/1b621961-3ae3-4dd2-9b1e-dba0ed2a0375)
