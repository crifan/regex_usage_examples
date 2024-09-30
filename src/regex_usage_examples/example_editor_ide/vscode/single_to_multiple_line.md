# 单行变多行加换行

想要从 [服务中心_查询保险条款题-条款内容页](http://www.epicc.com.cn/fuwu/chaxunbaoxiantiaokuan/cheliangbaoxian/201505/t20150507_2684.html) 复制出的文字：

```bash
【碰撞】指被保险机动车或其符合装载规定的货物与外界固态物体之间发生的、产生撞击痕迹的意外撞击。 【倾覆】指被保险机动车由于自然灾害或意外事故，造成本被保险机动车翻倒，车体触地，失去正常状态和行驶能力，不经施救不能恢复行驶。 【坠落】 指被保险机动车在行驶中发生意外事故，整车腾空后下落，造成本车损失的情况。非整车腾空，仅由于颠簸造成被保险机动车损失的，不属于坠落。 【外界物体倒塌】指被保险机动车自身以外的物体倒下或陷下。 【自燃】指在没有外界火源的情况下，由于本车电器、线路、供油系统、供气系统等被保险机动车自身原因或所载货物自身原因起火燃烧。 【火灾】指被保险机动车本身以外的火源引起的、在时间或空间上失去控制的燃烧（即有热、有光、有火焰的剧烈的氧化反应）所造成的灾害。 【次生灾害】指地震造成工程结构、设施和自然环境破坏而引发的火灾、爆炸、瘟疫、有毒有害物质污染、海啸、水灾、泥石流、滑坡等灾害。 【暴风】指风速在28.5米/秒（相当于11级大风）以上的大风。风速以气象部门公布的数据为准。 【暴雨】指每小时降雨量达16毫米以上，或连续12小时降雨量达30毫米以上，或连续24小时降雨量达50毫米以上。 【洪水】指山洪暴发、江河泛滥、潮水上岸及倒灌。但规律性的涨潮、自动灭火设施漏水以及在常年水位以下或地下渗水、水管爆裂不属于洪水责任。 【玻璃单独破碎】指未发生被保险机动车其他部位的损坏，仅发生被保险机动车前后风挡玻璃和左右车窗玻璃的损坏。 【车轮单独损坏】指未发生被保险机动车其他部位的损坏，仅发生轮胎、轮辋、轮毂罩的分别单独损坏，或上述三者之中任意二者的共同损坏，或三者的共同损坏。 【车身划痕损失】仅发生被保险机动车车身表面油漆的损坏，且无明显碰撞痕迹。 【新增设备】指被保险机动车出厂时原有设备以外的，另外加装的设备和设施。 【新车购置价】指本保险合同签订地购置与被保险机动车同类型新车的价格，无同类型新车市场销售价格的，由投保人与保险人协商确定。 【单方肇事事故】指不涉及与第三者有关的损害赔偿的事故，但不包括自然灾害引起的事故。 【家庭成员】指配偶、子女、父母。 【市场公允价值】 指熟悉市场情况的买卖双方在公平交易的条件下和自愿的情况下所确定的价格，或无关联的双方在公平交易的条件下一项资产可以被买卖或者一项负债可以被清偿的成交价格。
```

变成易读的，多行。

正则：

```bash
(【[^【】]+】)
\n$1
```

把：

【此处由于印象笔记冲突导致帖子图片丢失】

变成：

```bash

【碰撞】指被保险机动车或其符合装载规定的货物与外界固态物体之间发生的、产生撞击痕迹的意外撞击。
【倾覆】指被保险机动车由于自然灾害或意外事故，造成本被保险机动车翻倒，车体触地，失去正常状态和行驶能力，不经施救不能恢复行驶。 
【坠落】 指被保险机动车在行驶中发生意外事故，整车腾空后下落，造成本车损失的情况。非整车腾空，仅由于颠簸造成被保险机动车损失的，不属于坠落。 
【外界物体倒塌】指被保险机动车自身以外的物体倒下或陷下。 
【自燃】指在没有外界火源的情况下，由于本车电器、线路、供油系统、供气系统等被保险机动车自身原因或所载货物自身原因起火燃烧。 
【火灾】指被保险机动车本身以外的火源引起的、在时间或空间上失去控制的燃烧（即有热、有光、有火焰的剧烈的氧化反应）所造成的灾害。 
【次生灾害】指地震造成工程结构、设施和自然环境破坏而引发的火灾、爆炸、瘟疫、有毒有害物质污染、海啸、水灾、泥石流、滑坡等灾害。 
【暴风】指风速在28.5米/秒（相当于11级大风）以上的大风。风速以气象部门公布的数据为准。 
【暴雨】指每小时降雨量达16毫米以上，或连续12小时降雨量达30毫米以上，或连续24小时降雨量达50毫米以上。 
【洪水】指山洪暴发、江河泛滥、潮水上岸及倒灌。但规律性的涨潮、自动灭火设施漏水以及在常年水位以下或地下渗水、水管爆裂不属于洪水责任。 
【玻璃单独破碎】指未发生被保险机动车其他部位的损坏，仅发生被保险机动车前后风挡玻璃和左右车窗玻璃的损坏。 
【车轮单独损坏】指未发生被保险机动车其他部位的损坏，仅发生轮胎、轮辋、轮毂罩的分别单独损坏，或上述三者之中任意二者的共同损坏，或三者的共同损坏。 
【车身划痕损失】仅发生被保险机动车车身表面油漆的损坏，且无明显碰撞痕迹。 
【新增设备】指被保险机动车出厂时原有设备以外的，另外加装的设备和设施。 
【新车购置价】指本保险合同签订地购置与被保险机动车同类型新车的价格，无同类型新车市场销售价格的，由投保人与保险人协商确定。 
【单方肇事事故】指不涉及与第三者有关的损害赔偿的事故，但不包括自然灾害引起的事故。 
【家庭成员】指配偶、子女、父母。 
【市场公允价值】 指熟悉市场情况的买卖双方在公平交易的条件下和自愿的情况下所确定的价格，或无关联的双方在公平交易的条件下一项资产可以被买卖或者一项负债可以被清偿的成交价格。
```

方便拷贝到别处使用和阅读了。