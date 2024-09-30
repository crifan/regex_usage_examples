# 去掉srt字幕中font size

正则：

```bash
<font size="36">([^<>/]+)</font>
$1
```

从：

![vscode_srt_font_size_before](../../../assets/img/vscode_srt_font_size_before.png)

替换成：

![vscode_srt_font_size_after](../../../assets/img/vscode_srt_font_size_after.png)
