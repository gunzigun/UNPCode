# UNPCode
UNIX网络编程书籍1-8章的源码

下载: unpv13e.tar.gz 

解压: tar xvf unpv13e.tar.gz

进入到unpv13e目录

./lib/unp.h 中#include "../config.h"改成#include "config-unp.h"

./lib/unp.h 中#include "../lib/addrinfo.h"改成#include "addrinfo-unp.h"

./lib/unp.h 加一行 #define MAX_LINE 2048

cp ./lib/unp.h /usr/include/

mv config.h config-unp.h

mv ./lib/addrinfo.h ./lib/addrinfo-unp.h

cp ./config-unp.h /usr/include/

cp ./lib/addrinfo-unp.h /usr/include/

进入lib里make，生成libunp.a

cp ./libapue.a /usr/local/lib/

编译时链接到相应库: gcc -o 1-1 1-1.c -l unp

