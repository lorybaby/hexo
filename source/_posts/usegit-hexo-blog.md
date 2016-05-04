---
title: git hexo blog
date: 2016-05-01 14:41:19
tags: [git, hexo, blog]
description: "多台电脑同写一个gitblog"
---
## A电脑
先github创建一个库名为lorybaby.github.io， github它规定了此命名方式
命令终端里建立库作为博客用
``` bash
git config --global user.name "lorybby"
 git config --global user.email "lorybaby@126.com"
 git config --lis

 ssh-keygen -t rsa -C "lorybaby@126.com"
将 .ssh/*pub 复制到github  ---settings--SSH-add new ssh keys

ssh git@github.com
查看github的用户
cd  folder-yours
hexo init
npm install 
npm install hexo-deployer-git
hexo g -d 
发布失败看提升---git not found 则改 _config.yml 
deploy: #注意则里要有个空格 保留后再hexo d就通过了 这个算是hexo设计不合理吧
  type: git
  repo: git@github.com:lorybaby/lorybaby.github.io.git
  branch: master
hexo d  lorybaby.github.io查看博客

接着github创建hexo库来保存hexo文件下所有资料包括blog文件
echo "lll" >> README.md
git init
git add README.md
git commit -m "first commit"
 git remote add origin git@github.com:hex_blog
  fatal: remote origin already exists. 
 first
  git remote rm origin
  then 
 git remote add origin git@github.com:hex_blog

 git push -u origin master
```
现在 github 有2个库 一个是博客显示用  一个是所有配置文件存放用。

## In  B computer
接着用其它电脑就可以 git clone git@github.com:hexo到电脑本地接着写同一个博客
以后可以直接git  pull 新变化到本地
``` bash
npm install hexo-deployer-git --save
缺什么配置安装什么
注意新电脑里ssh key 添加到github上
写完博客后hexo g -d  or  hexo d 发布博客
最后把更新push
git add .
git commit -m "new change desk"
git push -u
##  Create a new post

``` bash
hexo new "new blog post"
hexo new page "new page about or something"


```
ssh git@github.com
hexo d 就不会有 host key的报错了  github 里的SSH里对应电脑的SHH钥匙会变亮了。
最后把变化更新备份到例外一个blog库里
git add .
git commit -m "this new change for blog"
 git remote add origin git@github.com:hex_blog
git push -u origin master

台式机写博客，先执行下面一种把笔记的更新合并到本地
``` bash
down vote
One approach is to commit that file first then pull.

git add filename
git commit 
//enter your commit message and save 
git pull 

Another approach is stash your changes then pull. Then apply stash.

git stash
git pull
git stash apply stash@{0}
```
然后台式电脑写好博客 hexo g -d 
## 简介命令
``` bash
hexo init
npm install 

npm install hexo-deployer-git --save  #有时候必须有save
hexo g -d

git init
git add .
git commit -m "laptop"
git remote add origin git@github.com:lorybaby/hexo
git push -u origin master
#此时可能会出错failed to push some refs to git  出现错误的主要原因是github中的README.md文件不在本地代码目录中，可以通过如下命令进行代码合并 因为GITHUB建库的时候初始化了README.md

git pull --rebase origin master
git push -u origin master

#B computer 换电脑都有重新配置hexo 部署环境
git clone git@github.com:lorybaby/hexo.git
cd hexo
npm install -g hexo-cli
npm install hexo-deployer-git --save
#如果不是第一次则
git pull
#写博客
hexo g -d
git add.
git commit -m "B news"
git push origin master


#git pull --rebase origin master 报错则
git status
git reset --hard 
``` 

