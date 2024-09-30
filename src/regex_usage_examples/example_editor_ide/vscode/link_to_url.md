# 把链接标题和地址变成Markdown中url格式

用：

```bash
^([^/]+)\n(https?://.+)
* [$1]($2)
```

把：

```bash
PyCharm Community Edition and Professional Edition Explained: Licenses and More | PyCharm Blog
https://blog.jetbrains.com/pycharm/2017/09/pycharm-community-edition-and-professional-edition-explained-licenses-and-more/
Differences between Pycharm community and professional edition?：Python
https://www.reddit.com/r/Python/comments/7370yp/differences_between_pycharm_community_and/
Pycharm的教育版和社区版有什么区别？ - 知乎
https://www.zhihu.com/question/47511825
使用PyCharm进行Python远程调试
http://leoc.leanote.com/post/remote-debugging-with-pycharm
Pycharm的远程代码编辑 - kiwik's blog
http://kiwik.github.io/python/2013/08/12/Pycharm的远程代码编辑/
```

变成markdown中url的格式：

```markdown
* [PyCharm Community Edition and Professional Edition Explained: Licenses and More | PyCharm Blog](https://blog.jetbrains.com/pycharm/2017/09/pycharm-community-edition-and-professional-edition-explained-licenses-and-more/)
* [Differences between Pycharm community and professional edition?：Python](https://www.reddit.com/r/Python/comments/7370yp/differences_between_pycharm_community_and/)
* [Pycharm的教育版和社区版有什么区别？ - 知乎](https://www.zhihu.com/question/47511825)
* [使用PyCharm进行Python远程调试](http://leoc.leanote.com/post/remote-debugging-with-pycharm)
* [Pycharm的远程代码编辑 - kiwik's blog](http://kiwik.github.io/python/2013/08/12/Pycharm的远程代码编辑/)

```
