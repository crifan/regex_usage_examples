# 去除掉csv中多余的`="xxx"`

客户给的一个数据文件csv格式的，但是内部内容中发现有多余的 `="xxx"`，应该改为`xxx`才对。

所以用VSCode去替换，用正则：

```bash
="(.+?)”
$1
```

实现了，把 `="7xxx1"`：

![vscode_remove_eaqual_quote_before](../../../assets/img/vscode_remove_eaqual_quote_before.png)

替换成 `7xxx1`：

![vscode_remove_eaqual_quote_after](../../../assets/img/vscode_remove_eaqual_quote_after.png)

即可。
