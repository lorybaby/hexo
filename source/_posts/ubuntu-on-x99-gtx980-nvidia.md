---
title: ubuntu on x99+ gtx980 nvidia
date: 2016-05-01 14:22:46
tags: [ubuntu, nvidia, cuda]
description: 小型工作站无HDI显示时输入信号超出频率范围的解决方式
---


小型工作站无HDI显示时，输入信号超出频率范围的解决方式: 
安装ubuntu 开始过程显示不正常 F6 字符串-- 前加入 nomodeset ，进入安装过程
准备按cuda_tookit安装包对应显卡型号，以及对应的最新显卡驱动，
安装完成后nvidia-settings 输入终端里 可以修改让显卡GPU0来承担显示功能，调整合适的分辨率，显示器也调整，ubuntu系统里显示也调整合适屏幕分辨率