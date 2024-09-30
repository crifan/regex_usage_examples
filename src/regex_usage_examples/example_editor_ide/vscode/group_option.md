# 正则的group的可选项

正则：

```bash
(\w+)\n+
($1)|
```

从：

```
debug
info
warning
warn
error
critical
exception
log

```

变成：

```c
(debug)|(info)|(warning)|(warn)|(error)|(critical)|(exception)|(log)|
```

用于后续正则表达式的group的可选项：

```py
    # logging.debug(
    # logging.warning(
    # logging.error(
    # logging.exception(
    CommonFunctionPList = [
        "logging\.((debug)|(info)|(warning)|(warn)|(error)|(critical)|(exception)|(log))",
。。。
    ]
    for curCommonFuncP in CommonFunctionPList:
        allCommonFunc = re.findall(curCommonFuncP, codeStr, re.I)
        curCommonFuncNum = len(allCommonFunc)
        specialKeyNum += curCommonFuncNum
```
