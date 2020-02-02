# JavaScript

代码：

```js
    let cowCodeRegex = new RegExp("/cowActivity/([^/]+)", "g");
    console.log(`cowCodeRegex=${cowCodeRegex}`);
    let foundCowCode = cowCodeRegex.exec(this.state.curUrl); ///uapp/cowActivity/12-0985/1/1522936800000
    console.log(`foundCowCode=${foundCowCode}`); ///cowActivity/13-6234,13-6234
    let cowCode = null;
    if (foundCowCode) {
      let inputStr = foundCowCode[0];
      console.log(`inputStr=${inputStr}`); ///uapp/cowActivity/11-5953
      cowCode = foundCowCode[1];
      console.log(`cowCode=${cowCode}`); //11-5953
    }
```

输出：

```bash
parsePageType: currentUrl=/uapp/cowActivity/12-0985/1/1522936800000 -> page=牛只活动量
index.js?5c2a:528 cowCodeRegex=/\/cowActivity\/([^\/]+)/g
index.js?5c2a:530 foundCowCode=/cowActivity/12-0985,12-0985
index.js?5c2a:534 inputStr=/cowActivity/12-0985
index.js?5c2a:536 cowCode=12-0985
index.js?5c2a:540 fullTitle=牛只活动量 12-0985
```
