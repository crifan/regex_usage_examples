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

详见：

【整理Book】主流文档型数据库：MongoDB
