# 编译注意事项

该工程是使用VS2022 + CMake 编译的

编译过程中有几个问题

1.是triangle.c中有一段注释，如果使用非unix系统，需要添加`#define NO_TIMER`指令, 我基于此加上了`#ifndef __UNIX__`指令用于判断系统

2.原本的SWAP_io.c中，有一段

```c
#ifdef WIN32
#include <sys/time.h>
//...
```

修改为：

```c
#ifdef WIN32
#include <time.h>
//...
```

3.Debug模式编译的mcf.exe直接执行，不会弹出任何消息, 但Release可正常使用，不确定是不是哪里有问题，