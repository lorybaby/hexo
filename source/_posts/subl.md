---
title: sublime with markdown
date: 2016-05-28 14:41:19
tags: [sublime, markdown]
description: "sublime用的到的技巧,以及markdown介绍。"
---
## sulbime markdow highlight
1. install Monokai Extended pacakge and select the Monokai Extended color scheme
2. install The Markdown Extended Package and enjoy language-specific syntax highlighting
安装完毕 ctrl+shift+p  单词首字母ssme (set syntax:Markdown Extended) 快速切换highlighting mode.

## markdown 语法简介
直接以hexo主题为例：
### Introduction 前言
```
Theme **Yelee** 用黑体 relies on [Hexo-Theme-Yilia][1], thanks for the author [Litten][2]. Fix some bugs, change lots of styles, add several features. And then I made the theme. Yelee is mainly designed for fluent text reading. I change styles and add functions, meanwhile, try hard to keep this theme simple, stupid and clear. Theme DEMO: [MOxFIVE's Blog][6]

> 使用段落快
链接也可以直接follow: e.g [Preview](http://hexo.io/hexo-theme-landscape/),但是用上面的方式好处是可以重复使用
简单的代号代表，类似SCI文章里的参考文献使用。
```
> M-Hexo-Blog [Commits][3]; hexo-theme-yelee [Commits][4]; [建站日志][5]

[1]: https://github.com/litten/hexo-theme-yilia
[2]: http://litten.github.io/ "Litten的博客"
[3]: https://github.com/MOxFIVE/M-Hexo-Blog/commits/master
[4]: https://github.com/MOxFIVE/hexo-theme-yelee/commits/master
[5]: http://moxfive.xyz/2015/08/20/blog-building/ "个人博客站点建设历程"
[6]: http://moxfive.xyz
[1~6] 这些links不会被显性
```
### New Features 新特性
| - |            Chs           |                En               |
|:-:|:------------------------:|:-------------------------------:|
| 1 | 嵌入边栏的文章目录       | Flexible table of contents      |
| 2 | 透明化背景，随机背景大图 | Transparent & Random background |
| 3 | 页内跳转按钮             | Scrolling button                |
| 4 | 文章版权等信息显示       | Copyright info.                 |
| 5 | 文章导航切换按钮         | Post navigation button          |
| 6 | 网站计数                 | Site counter                    |
| 7 | 多语言支持                 | i18n, multi-language          |

表格使用
“```”不指定语言模式 效果类似段落块
```

`单独的字体加背景块` 用``    ![图片](https://github.com/lorybaby/lorybaby.github.io/tree/master/img/test.png)
``` yml 
``` yml bash python hightlight何种语言 
[Hexo-Theme-Yilia][1]
[Hexo-Theme-Yilia](https://github.com/litten/hexo-theme-yilia)
[1]: https://github.com/litten/hexo-theme-yilia
two link forms
![图片](https://github.com/lorybaby/lorybaby.github.io/tree/master/img/test.png)
notice "!" convert to picture not links
```
## 主题更新
``` git
cd themes/yelee
git pull
error: Your local changes to the following files would be overwritten by merge:
        _config.yml
        layout/_partial/footer.ejs
Please, commit your changes or stash them before you can merge.
Aborting

Commit the change using
git commit -m "My message"
git pull
or 重命名原来的文件 比较pull后差异 在决定添加更改
```

## hexo-generator-search
会生成一个 search.xml 文件方便添加搜索功能, [**我尝试并没有成功，后期还需要探索下**](http://hahack.com/codes/local-search-engine-for-hexo/)

Generate search data for Hexo 3.0. This plugin is used for generating a search.xml file, which contains all the neccessary data of your articles that you can use to write a local search engine for your blog.

安装 $ npm install hexo-generator-search --save

修改 _config.yml

search:
  path: search.xml
  field: post
不过这个功能需要自己配置另外的服务器，比如搭建在 SAE 之类的，所以暂时也先不折腾