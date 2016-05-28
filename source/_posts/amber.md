---
title: amber skills notices
date: 2016-05-26 14:41:19
tags: [amber,MD,sdg,bash]
description: "amber MD"
---
## AMBER 会重给PDB编号
1.amber有 它命名的规则，都是重1开始增加无论单链or多链，而且AB链也不会有相同的number
amber 和sdg联用可以确保启始构象达到最合理化，sdg  prep Wiz 可以帮助检测原子的键数是否正确，有没有gap等等。
值得注意的是 sdg 默认loop建模并不一定合理，可以再次prep Wiz 检测 原子重叠情况越多越不合理。
2.tleap 保存 pdb时 即使水分子本来排序在B链之前，保存后所有的水分子 离子等都会排序在AA后面，所以加限制时一定要搞清number,
这也许是amber 自有的命名规则导致的缺陷。


##  AMBER 改in文件
1.通常不同.in文件有同样的参数，比如同样的限制标记符号 ntr=1, restraintmask=':1-346', 需要改成 ':1-368'
命令： sed -i "s/:1-346/:1-368/g" `grep :1-346 -rl ./in`

比如，要将目录in下面所有文件中的zhangsan都修改成lisi，向上那样
替换：s命令  
     $ sed 's/test/mytest/g' example-----在整行范围内把test替换为mytest。如果没有g标记，则只有每行第一个匹配的test被替换成mytest。
     -i 表示inplace edit，就地修改文件
-r 表示搜索子目录
-l 表示输出匹配的文件名
这个命令组合很强大，要注意备份文件。

## 用高斯计算电荷单点能
如果小分子配体.pdb 中有原子如H4' ，C2', 高斯会生成.com中的原子对应加 H4d , C2P 等 目前还不知道含义是什么？