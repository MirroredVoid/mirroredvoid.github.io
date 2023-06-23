---
title: 帖子中插入音频播放测试页
description: 
slug: first-post
date: 2023-06-14T12:59:40Z
image: CoverTest.jpg
categories:
    - 虚拟歌姬
tags:
    - 含音频
---

测试帖子
![Image 1](RenshiCover.jpg)
此处放一个一个一个一个一个音频测试+623

1.直接放音乐播放器：
​<audio id="aa" controls="" preload="none" style="width:100%">
      <source id="mp3" src="Renshi_MixingF.mp3">
</audio>

2.用一个按钮触发音频
<span class='article-category'>
<a href="#" onClick="var au=document.getElementById('aa');au.play()">12345</a>
<a href="#" onClick="var au=document.getElementById('aa');au.play()" style="background-color: #66bb6a;">67890</a>
</span>

3.点击图片触发音频
<span class='article-category'>
<a href="#" onClick="var au=document.getElementById('aa');au.play()" style="width:40%">
    <img src="RenshiCover.jpg"></img>
</a>
</span>

>备用

# 备用
## 备用
### 备用
---
***
