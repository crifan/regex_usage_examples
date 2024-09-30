# 给文章段落增加换行

用正则：

```bash
\n(\d.)
\n\n$1
```

把：

```bash
...互。
1.字节跳动
...说过。
2.陆奇给年轻人的话
...
8.网易 丁磊
...
```

![vscode_para_no_newline_before](../../../assets/img/vscode_para_no_newline_before.png)

变成：

```bash
...互。
1.字节跳动
...说过。

2.陆奇给年轻人的话
...

8.网易 丁磊
...
```

![vscode_para_no_newline_after](../../../assets/img/vscode_para_no_newline_after.png)
