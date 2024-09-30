# 把url中query parameter分出来

折腾：

【未解决】爬取mp.codeup.cn中的英语教材电子书资源

期间，对于：

```bash
http://mp.codeup.cn/book/sample2.htm?id=52365&shelfId=4824&share_=6765370&sh=sh&vt_=1583111113754&_logined=1
```

想要把参数分出来

用正则：

```bash
[&?](.+?)=([^&=]+)
\n$1 = $2
```

从：

【此处由于印象笔记冲突导致帖子图片丢失】

变成：

```bash
http://mp.codeup.cn/book/sample2.htm
id = 52365
shelfId = 4824
share_ = 6765370
sh = sh
vt_ = 1583111113754
_logined = 1
```

除了第一行，剩下的就是我们要的`key=value`形式了。
