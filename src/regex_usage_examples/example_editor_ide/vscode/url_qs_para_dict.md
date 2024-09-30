# 把url中查询参数换成代码中字典参数

用正则：

```bash
dt=([^&]+)&?
"dt": "$1",\n
```

把：

```bash
dt=at&dt=bd&dt=ex&dt=ld&dt=md&dt=qca&dt=rw&dt=rm&dt=ss&dt=t
```

![vscode_http_queray_para_before](../../../assets/img/vscode_http_queray_para_before.png)

替换成：

```bash
"dt": "at",
"dt": "bd",
"dt": "ex",
"dt": "ld",
"dt": "md",
"dt": "qca",
"dt": "rw",
"dt": "rm",
"dt": "ss",
"dt": "t",
```

![vscode_http_queray_para_after](../../../assets/img/vscode_http_queray_para_after.png)

用于后续放到代码中使用：

![http_para_dict_in_code](../../../assets/img/http_para_dict_in_code.png)
