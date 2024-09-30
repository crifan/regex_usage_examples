# 把print换成logging.debug

用：

```bash
print\("([^"]+)"(\s*%\s*\(?([^\)]+)\)?)?\)
logging.debug("$1", $3)
```

把：

print没有参数的：

```python
print("taped 通讯录")
```

print单个参数的

```python
print("++++++++++ taped element: %s" % curElement)
```

print多个参数的：

```python
print("++++++++++ clicked element position: %s,%s" % (centerX, centerY))
print("Cost time %.2fs for save source %s" % (saveSourceTime, savedSourceFile))
```

都一次性变成logging.debug的写法：

```python
      logging.debug("++++++++++ taped element: %s", curElement)

      logging.debug("++++++++++ clicked element position: %s,%s", centerX, centerY)

    logging.debug("Cost time %.2fs for save source %s", saveSourceTime, savedSourceFile)

    logging.debug("taped 通讯录", )
```
