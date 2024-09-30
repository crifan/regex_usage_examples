# 去除每行秒及毫秒的多余换行

正则：

```bash
\n((\d+ s )?\d+ ms)
$1
```

从：

```bash
completed successfully 
3 s 149 ms 
Run build 
3 s 80 ms 
Load build 
2 ms 
Evaluate settings 
1 ms 
Finalize build cache configuration 


Configure build 
420 ms 
Load projects 
6 ms 
Calculate task graph 
120 ms 
Run tasks 
2 s 532 ms 
:api:preBuild 
21 ms 
:api:preDebugBuild 
3 ms 
:api:compileDebugAidl 
1 s 95 ms 
Execute taskAction 
869 ms 
:cts_provider:preBuild 

。。。
```

变成：

```bash
completed successfully 3 s 149 ms 
Run build 3 s 80 ms 
Load build 2 ms 
Evaluate settings 1 ms 
Finalize build cache configuration 


Configure build 420 ms 
Load projects 6 ms 
Calculate task graph 120 ms 
Run tasks 2 s 532 ms 
:api:preBuild 21 ms 
:api:preDebugBuild 3 ms 
:api:compileDebugAidl 1 s 95 ms 
Execute taskAction 869 ms 
:cts_provider:preBuild 
。。。
```

即可实现：

去掉了每行多余的换行
