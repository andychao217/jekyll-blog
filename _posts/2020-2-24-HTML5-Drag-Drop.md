---
layout: post
title: HTML5中Drag & Drop拖曳效果的用法
---

```HTML
缺乏对clearData() dropEffect() effectAllowed()的理解

eg1:
把图像放在边框中
<!DOCTYPE HTML>
<html>
<head>
<meta charset="utf-8">
<style type="text/css">
#div1 {width:198px; height:66px;padding:10px;border:2px solid #aaaaaa;}
</style>
<script type="text/javascript">
function allowDrop(ev)
{
ev.preventDefault();
}


function drag(ev)
{
ev.dataTransfer.setData("img",ev.target.id);
}


function drop(ev)
{
ev.preventDefault();
var data=ev.dataTransfer.getData("img");
ev.target.appendChild(document.getElementById(data));
}
</script>
</head>
<body>


<p>请把 W3School 的图片拖放到矩形中：</p>
<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
<br/>
<img id="drag1" width="100px" height="50px" src="drag.jpg" draggable="true" ondragstart="drag(event)"/>
</body>
</html>


eg2:图片在两个边框之中来回拖放
<!DOCTYPE HTML>
<html>
<head>
<style type="text/css">
#div1, #div2
{float:left; width:198px; height:66px; margin:10px;padding:10px;border:1px solid #aaaaaa;}
</style>
<script type="text/javascript">
function allowDrop(ev)
{
ev.preventDefault();
}


function drag(ev)
{
ev.dataTransfer.setData("Text",ev.target.id);
}


function drop(ev)
{
ev.preventDefault();
var data=ev.dataTransfer.getData("Text");
ev.target.appendChild(document.getElementById(data));
}
</script>
</head>
<body>


<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)">
  <img src="/i/eg_dragdrop_w3school.gif" draggable="true" ondragstart="drag(event)" id="drag1" />
</div>
<div id="div2" ondrop="drop(event)" ondragover="allowDrop(event)"></div>


</body>
</html>
```
