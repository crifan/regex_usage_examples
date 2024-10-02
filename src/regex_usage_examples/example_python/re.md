# re

Python中有专门的正则的模块：

* 概述
  * Python中的re模块
    * 文档
      * 中文
        * [re --- 正则表达式操作 — Python 3.12.7 文档](https://docs.python.org/zh-cn/3/library/re.html#regular-expression-syntax)
      * 英文
        * [re — Regular expression operations — Python 3.12.7 documentation](https://docs.python.org/3/library/re.html#regular-expression-syntax)
    * 常用函数
      * 通用
        * 编译表达式
          * `re.compile`
            * `re.compile(pattern, flags=0)`
      * 查找
        * `re.search`
          * `re.search(pattern, string, flags=0)`
        * `re.findall`
          * `re.findall(pattern, string, flags=0)`
      * 匹配
        * `re.match`
          * `re.match(pattern, string, flags=0)`
      * 替换
        * `re.sub`
          * `re.sub(pattern, repl, string, count=0, flags=0)`
* 详解
  * [Python中正则表达式：re模块详解](http://book.crifan.org/books/python_regex_re_intro/website)
