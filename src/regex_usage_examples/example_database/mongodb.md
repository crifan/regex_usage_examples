# MongoDB

相关代码：

```python
if args.get('title'):
    filters['title'] = {'$regex': args['title'], '$options': 'i'}

if args.get('unitCode'):
    filters['unit_code'] = {'$regex': args['unitCode'], '$options': 'i'}
```

其中的`$regex`表示搜索时，用正则搜索

-》此处含义是：去搜索`title`和`unitCode`两个字段，且`i`表示不区分大小写
