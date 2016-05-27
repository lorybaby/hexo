---
title: built protien model and amber MD
date: 2016-05-26 14:41:19
tags: [sdg,moldeller,amber]
description: "蛋白建模"
---
## license MODELIRANJE
需要注意的是easymodel 要求modeller 安装到默认目录c:\Program Files
若是linux版本 使用命令mod9.16
## sdg 
modeller 免费但是用起来需要有python常识，不是很友好，如果有薛定谔那就很方便了，
sdg--同源建模--predict structure

## 在晶体结构基础上修复N段缺失部分
1.AB链对称，需要在AB的N两末端都加几个氨基酸，我的做法是AB链分别建模然后合并。----更简单是选择Multi-template model type: Homo-multimer
这样同一目标序列（query sequnce on every template simultaneously)更具模板的空间坐标同时建模。
2.同一条链由不同模板构成  同上Multi-template model type: Composite/Chimera 鼠标选择要选的序列。
其实完全可以用重建模的方式突变or添加AA，以原晶体结构为模板，将更改的原序列为目标序列建模。
3.

















































