# 只保留游戏名后加上顿号

正则：

```bash
[\w\.]+/([^\|/]+)\|http.+\s*
$1、
```

把：

```bash
com.sy.fsyhj.vivo/浮生妖绘卷|https://gameapkbddl.vivo.com.cn/appstore/developer/soft/20201022/202010221943274reut.apk
com.aiyou.jianzongqy.vivo/剑踪情缘|https://gameapktxdl.vivo.com.cn/appstore/developer/soft/20201019/202010191206022ecy5.apk
com.youyan.xszn.vivo/仙神之怒|https://gameapkbddl.vivo.com.cn/appstore/developer/soft/20200519/202005191821212583555.apk
com.cmcx.xjhsl.vivo/仙界幻世录|https://gameapktxdl.vivo.com.cn/appstore/developer/soft/20190531/201905311652384109085.apk
com.game.hundunxmj.vivo/混沌仙魔诀|https://gameapktxdl.vivo.com.cn/appstore/developer/soft/20200518/202005181552511906386.apk
com.shjs.jzxjz.vivo/九州仙剑传|https://gameapktxdl.vivo.com.cn/appstore/developer/soft/20200302/202003021054228210141.apk
com.yzcm.xxsj.vivo/修仙世界|https://gameapktxdl.vivo.com.cn/appstore/developer/soft/20200624/202006241643504389947.apk
com.taifeng.tiantu.vivo/天途|https://gameapktxdl.vivo.com.cn/appstore/developer/soft/20201111/2020111111561015xkf.apk
com.xianmoji.jundao.vivo/仙魔纪|https://gameapktxdl.vivo.com.cn/appstore/developer/soft/20201126/2020112615414443ji7.apk
com.junhai.txd.vivo/天行道|https://gameapk.vivo.com.cn/appstore/developer/soft/20200424/202004240926143484604.apk
com.idreamsky.jzmf.vivo/决战玛法|https://gameapkbddl.vivo.com.cn/appstore/developer/soft/20200814/202008141614516937557.apk
com.sdg.woool.guaji.vivo/传世挂机|https://gameapktxdl.vivo.com.cn/appstore/developer/soft/20190411/201904111747598508259.apk
com.game.qianyou.molj.vivo/魔龙诀|https://gameapkbddl.vivo.com.cn/appstore/developer/soft/20201014/202010141220276qt5a.apk
com.game.huangchengcqi.vivo/皇城传奇|https://gameapk.vivo.com.cn/appstore/developer/soft/20200601/202006011847591164920.apk
com.whtt.zzcq.vivo/主宰传奇|https://gameapktxdl.vivo.com.cn/appstore/developer/soft/20200108/202001081542347512628.apk
com.snda.sbkcq2.vivo/沙巴克传奇|https://gameapkbddl.vivo.com.cn/appstore/developer/soft/20200622/202006221140177296978.apk
com.sj.sbcq.vivo/双倍传奇|https://gameapktxdl.vivo.com.cn/appstore/developer/soft/20200214/202002141238155814708.apk
com.cqzzdlq.vivo/传奇至尊|https://gameapk.vivo.com.cn/appstore/developer/soft/20191227/20191227164042177531.apk
com.yzcm.cqbz.vivo/完美传奇|https://gameapkbddl.vivo.com.cn/appstore/developer/soft/20201111/202011111458575lhps.apk
com.game.qianyou.skzm.vivo/时空之门|https://gameapk.vivo.com.cn/appstore/developer/soft/20201130/202011301437159gwc7.apk
```

替换成：

```bash
浮生妖绘卷、剑踪情缘、仙神之怒、仙界幻世录、混沌仙魔诀、九州仙剑传、修仙世界、天途、仙魔纪、天行道、决战玛法、传世挂机、魔龙诀、皇城传奇、主宰传奇、沙巴克传奇、双倍传奇、传奇至尊、完美传奇、时空之门、
```

用途：粘贴到别处，表示已处理的游戏列表
