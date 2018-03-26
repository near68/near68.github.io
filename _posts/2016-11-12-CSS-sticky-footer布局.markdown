---
layout: post
title:  "CSS sticey footer布局"
date:   2016/11/12 20:00:00
categories: CSS
---
相关教程[w3cplus-CSS秘密花园： Sticky footers](https://www.w3cplus.com/css3/css-secrets/sticky-footers.html)

目的：
    模块永远占满视口，页面内容不够长时，关闭按钮在视窗底部；如果内容足够长时，页脚块会被内容向下推送。

HTML

```

<div class="container">
    <div class="content-wrapper>
       <div class="content">内容区域，可随机长度</div>
    </div>
    <div class="close">
<div>


```

CSS

```

.container{//总容器为全屏，所以高度为100％
  positon: fiexd;
  top:0;
  left:0;
  height:100%;
  overflow: auto;//如果内容太长，会显示滚动条查看其余内容。
 }
.content-wrapper{
  min-height: 100%;//如果内容不够长时，也保证内容有全屏长度
}
.content{
  margin-top: 50px;//向上和屏幕顶部保持50px间距
  padding-bottom: 50px;//保证内容content区域的底部有50px的空白
}
.close{
   margin: -64px;//让关闭按钮向content－wrapper里面伸入50px，正好把内容区的50px空白补上；
}

```
