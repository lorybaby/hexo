---
title: pymol skills
date: 2016-05-19 14:41:19
tags: [pymol]
description: "pymol用的到的技巧"
---
## pymol cmd
``` bash
load com.top,mov,format=top      ###pymol要求载入轨迹前要先载入拓扑文件，除非后缀是top，后缀是prmtop的话除非定义一下格式，否则是不认的（不知是不是只有我有这个情况）
load_traj head.crd,mov,format=trj   

mset 1 x60              ;
# define a movie of 60 frames
util.mrock(1,60,60,1,1) ;
# issues mdo commands to create -/+ 60 deg. rock over 60 frames
set ray_trace_frames=1  ;
# whether or not ray each frame （0 - don ray each frame)
set cache_frames=1      ;
# whether or not PyMOL saves frames in memory
mplay                   ;
# play the movie
mpng mov                ;
# will create mov0001.png, mov0002.png, ... mov0060.png.


#pymol 
set ray_shadows,off  # turn off shadows
```