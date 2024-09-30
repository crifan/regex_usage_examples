# 去除内容中多余的 lessionxxx的单词

正则：

```bash
lesson\s*\d+\n

```

从：

![vscode_lessonxxx_before](../../../assets/img/vscode_lessonxxx_before.png)

替换成：

![vscode_lessonxxx_after](../../../assets/img/vscode_lessonxxx_after.png)

### 语句末尾去掉感叹号

正则：

```bash
!\n
\n
```

从：

![vscode_line_end_exclamation_before](../../../assets/img/vscode_line_end_exclamation_before.png)

替换成：

![vscode_line_end_exclamation_after](../../../assets/img/vscode_line_end_exclamation_after.png)
