# VSCode

## VSCode中正则语法说明

* 替换中引用搜索中的分组
  * 背景：搜索带`分组`
    * 写法：`(xxx)`
  * 语法：替换时引用对应分组，用：`$N`
    * N=1,2,3,...
  * 举例
    * 例子
      * 搜索：`(\w+)\n`
      * 替换：`"$1",\n`
* 环视
  * 可以参考自己的教程
    * [环视断言 · 应用广泛的超强搜索：正则表达式](https://book.crifan.com/books/super_search_regex/website/regex_syntax/look_around/)
  * 核心要点和举例
    * `(?=xxx): (positive) look ahead (assertion)=正向肯定断言`
    * `(?!xxx): negative look ahead (assertion)=正向否定断言`
    * `(?<=xxx): (positive) look behind (assertion)=反向肯定断言`
      * 例子1：
        ```bash
        (?<!\s)<([\.\w]+)>
        &lt;$1&gt;
        ```
    * `(?<!xxx): negative look behind (assertion)=反向否定断言`
      * 例子1
        ```bash
        (?<!http\.)get\(
        ```
      * 例子2
        ```bash
        (?<!")15(?!")
        ```
