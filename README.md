# inject-to-branch
if-else根据AST寻找行号，然后对源代码文件插入，　AST使用libclang生成(不能直接用clang的命令行参数生成，行号不对，只在app.c的情况下不对)

switch-case 直接字符串查找case行，在:后面加入即可

运行
```shell
python modify_src2.py file.c
```
```c
printf("hello");
```
即可生成对应插桩的injected.c文件
代码粗糙，无需优化

