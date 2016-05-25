---
title: R,Rstudio install
date: 2016-05-22 14:41:19
tags: [R]
description: "R源安装最新版以及RStudio"
---

``` bash
sudo apt-get build-dep r-base
如果不先安装好依赖包将会麻烦不断 比如不能和Rstudio联用 最后不能生成pdf 等
./configure --prefix=$HOME/R/R-3.3.0 --enable-R-shlib --with-blas --with-lapack
blas  speed up calculations that are common in many analytic methods.
make
sudo make install
sudo ln -s /opt/R/3.2.3/bin/R /bin/R 

Finally, after you have installed R, you might want to check that it was compiled with all your desired capabilities (e.g. png, cairo, tcltk, etc.) with this command:

> capabilities()
```