# 想要搜索15秒相关的内容

直接搜15，找到很多`xxx="15"`不是我们要的：

【此处由于印象笔记冲突导致帖子图片丢失】

所以想要排除掉：

* 前面是双引号
* 后面也是双引号的

所以用：

```bash
(?<!")15(?!")
```

即可过滤掉，找到其他地方的15：

【此处由于印象笔记冲突导致帖子图片丢失】

即，支持用

* `look ahead negative`
* `look behind negative`

去过滤掉不要的情况。