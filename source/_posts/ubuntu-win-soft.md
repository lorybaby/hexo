---
title: ubuntu win soft
date: 2016-05-04 15:18:58
tags: [win, ubuntu, soft]
description: "ubuntu工作站软件配置"
---

## 配置安装foxit Reader
安装好wine
找foxit 阅读器  这里使用的是7.0版本绿色免安装 win7 下解压安装好 直接考到ubuntu里
不要随意改变foxit文件夹ubuntu里的位置
then  change the foxitReader style 



## bashrc 记录
``` bash

export WOR=$HOME/work
export PRO=$HOME/pro


#cuda
export CUDA_HOME=/usr/local/cuda-7.5
export PATH=$PATH:$CUDA_HOME/bin
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CUDA_HOME/lib64
#amber
export AMBERHOME=$PRO/amber14
export PATH=$PATH:$AMBERHOME/bin
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$AMBERHOME/lib
#FOR  gv
export GV_DIR=$PRO/g09/gview
export LIBPATH=$PRO/g09/gview
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$PRO/g09/gview/lib
export PATH=$PATH:$PRO/g09/gview
alias gv='gview.exe'
#for guassian
export g09root=$PRO/g09
export GAUSS_SCRDIR=$PRO/g09/scratch
export PATH=$PATH:$g09root
source $PRO/g09/bsd/g09.profile
#for java
export JAVA_HOME=/usr/lib/jvm/java-7-openjdk-amd64
export PATH=$PATH:/usr/lib/jvm/java-7-openjdk-amd64/bin
#for sdg
export SCHRODINGER=/home/lory/pro/sdg
export PATH=$PATH:$SDG_HOME

#for foxitReader
export PATH=$PATH:$HOME/pro/Foxit Reader

alias opendir='nautilus'
alias sopendir='sudo nautilus'
alias sdg=\$SCHRODINGER/maestro
```
