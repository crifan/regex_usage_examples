# BeautifulSoup

`BeautifulSoup`中的`find`和`findAll`的`name`或`attr`参数，支持正则写法：

代码：

```python
h1userSoupList = soup.findAll(name="h1", attrs={"class":re.compile(r"h1user(\s\w+)?")});
```

可以从html：

```html
<div class="icon_col">
        <h1 class="h1user">crifan</h1>
        <h1 class="h1user test1">crifan 123</h1>
        <h1 class="h1user test2">crifan 456</h1>
</div>
```

搜到列表：

```bash
class="h1user"
class="h1user test1"
class="h1user test2"
```
