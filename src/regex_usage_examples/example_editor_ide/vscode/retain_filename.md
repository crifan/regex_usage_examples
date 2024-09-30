# 去掉其他只保留文件名

正则：

```bash
\[.+?\]\t(.+.((jpg)|(png)|(gif)|(pdf))).+\n*
$1\n
```

从：

```bash
[IMG]    主流测试工具分类.jpg    2018-09-21 20:59    159K     
[IMG]    内网渗透.png    2020-02-03 01:25    265K     
[IMG]    域名搜集途径.png    2018-09-21 20:59    139K     
[IMG]    安全漏洞总结.jpg    2018-09-21 20:59    368K     
[IMG]    密码找回逻辑漏洞总结.png    2018-12-18 05:09    141K     
[IMG]    渗透标准.jpg    2020-02-03 01:25    189K     
[IMG]    渗透流程.jpg    2018-09-21 20:59    56K     
[IMG]    渗透测试实验室.jpg    2020-02-03 01:25    888K     
[IMG]    渗透测试思维导图.png    2020-02-03 01:25    3.7M     
[IMG]    渗透测试流程.jpg    2018-09-21 20:59    221K     
[IMG]    渗透测试详细版.jpg    2018-09-21 20:59    260K     
[IMG]    社会工程学.jpg    2018-09-21 20:59    95K     
[IMG]    系统端口审计琐事.jpg    2018-09-21 20:59    57K     
[IMG]    网站入侵图.jpg    2018-09-21 20:59    92K     
[IMG]    网络安全绪论.png    2018-09-21 20:59    678K     
[IMG]    进阶渗透.png    2018-09-21 20:59    103K     
[IMG]    黑客入侵行为分析.gif    2018-09-21 20:59    18K     
[IMG]    JavaWeb简介.png    2018-09-21 20:59    913K     
[IMG]    Jboss引起的内网渗透.png    2018-09-21 20:59    229K     
[IMG]    Maltego使用导图.jpg    2018-09-21 20:59    539K     
[IMG]    Nmap.png    2018-09-21 20:59    1.1M     
[IMG]    PHP源码审计.png    2018-09-21 20:59    4.0M     
[   ]    PTES_MindMap_CN1.pdf    2018-09-21 20:59    417K     
[IMG]    Python系统审计.jpg    2018-09-21 20:59    343K     
[IMG]    RedTeamManula.jpg    2020-02-03 01:25    5.8M     
[IMG]    WEB2HACK.jpg    2020-02-03 01:25    137K     
[IMG]    Web安全技术点.jpg    2018-09-21 20:59    193K     
[IMG]    Web安全.png    2018-09-21 20:59    228K     
[IMG]    Web指纹分析方法.png    2018-09-21 20:59    55K     
[IMG]    Web攻击及防御技术.png    2018-09-21 20:59    855K     
[IMG]    Web服务器入侵防御.jpg    2018-09-21 20:59    88K     
[IMG]    Web 架构中的安全问题.png    2018-09-21 20:59    728K     
[IMG]    Windows常见持久控制.png    2020-02-03 01:25    185K     
[IMG]    XSS利用架构图.jpg    2020-02-03 01:25    100K     
[IMG]    XSS攻击点汇总.png    2018-09-21 20:59    2.2M     
[IMG]    nmap.jpg    2018-09-21 20:59    295K     
[IMG]    pentest_method.jpg    2018-09-21 20:59    177K     
[IMG]    pentester.jpg    2018-09-21 20:59    3.6M     
[IMG]    powershell语法.png    2018-09-21 20:59    323K     
[IMG]    web应用测试.jpg    2020-02-03 01:25    607K     
[IMG]    web渗透.jpg    2018-09-21 20:59    225K     
[IMG]    xml安全汇总.png    2018-09-21 20:59    1.7M     
```

替换为：

```bash
主流测试工具分类.jpg
内网渗透.png
域名搜集途径.png
安全漏洞总结.jpg
密码找回逻辑漏洞总结.png
渗透标准.jpg
渗透流程.jpg
渗透测试实验室.jpg
渗透测试思维导图.png
渗透测试流程.jpg
渗透测试详细版.jpg
社会工程学.jpg
系统端口审计琐事.jpg
网站入侵图.jpg
网络安全绪论.png
进阶渗透.png
黑客入侵行为分析.gif
JavaWeb简介.png
Jboss引起的内网渗透.png
Maltego使用导图.jpg
Nmap.png
PHP源码审计.png
PTES_MindMap_CN1.pdf
Python系统审计.jpg
RedTeamManula.jpg
WEB2HACK.jpg
Web安全技术点.jpg
Web安全.png
Web指纹分析方法.png
Web攻击及防御技术.png
Web服务器入侵防御.jpg
Web 架构中的安全问题.png
Windows常见持久控制.png
XSS利用架构图.jpg
XSS攻击点汇总.png
nmap.jpg
pentest_method.jpg
pentester.jpg
powershell语法.png
web应用测试.jpg
web渗透.jpg
xml安全汇总.png
```
