# 搜索get函数被调用的地方

默认如果搜

```bash
get(
```

则会搜出来很多，有很多个 我们不希望看到的

```bash
http.get(
```

想要排斥掉`http.get(`

想到了用正则

参考之前语法：

`(?<!xxx): negative look behind (assertion)=反向否定断言`

去用：

```bash
(?<!http\.)get\(
```

然后只有7个，都是我们要找到了：

【此处由于印象笔记冲突导致帖子图片丢失】
