# 填充Markdown中图片文件名

此处正在写教程期间，正好有个需求：为了避免和消除Markdown中的，关于图片的文件名即image的alt的text是空的警告：

![markdown_img_alt_empty_warning](../../../assets/img/markdown_img_alt_empty_warning.png)

然后正好用正则，去自动填充此处image的alt的text，即图片的文件名

用正则：

```bash
!\[\]\(\.\./\.\./assets/img/([^/]+)\.(\w{3})\)
![$1](../../../assets/img/$1.$2)
```

把：

```bash
![sublime_2nd_findall](../../../assets/img/sublime_2nd_findall.png)

![sublime_2nd_replaced](../../../assets/img/sublime_2nd_replaced.png)

![regex_all_city_to_xmind](../../../assets/img/regex_all_city_to_xmind.png)
```

![vscode_markdown_img_alt_before](../../../assets/img/vscode_markdown_img_alt_before.png)

变成：

```bash
![sublime_2nd_findall](../../../assets/img/sublime_2nd_findall.png)

![sublime_2nd_replaced](../../../assets/img/sublime_2nd_replaced.png)

![regex_all_city_to_xmind](../../../assets/img/regex_all_city_to_xmind.png)
```

![vscode_markdown_img_alt_after](../../../assets/img/vscode_markdown_img_alt_after.png)

即可自动填充image的alt的text，消除Markdown中的警告了。
