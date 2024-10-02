# MongoDB Compass

`MongoDB Compass`中想要用正则搜索字段：

```js
grading
    lexile: "AD450L"
```

写法是：

```js
{"grading.lexile": {$regex: "AD.*"}}
```

或：regex加上行首和行尾判断：

```js
{"grading.lexile": {$regex: "^AD.*$"}}
```

或 regex用引号引起来

```js
{"grading.lexile": {"$regex": "AD.*"}}
```

具体详见：

[高级搜索 · 主流文档型数据库：MongoDB (crifan.org)](https://book.crifan.org/books/popular_document_db_mongodb/website/summary_note/record/find_query/advanced.html)

