---
layout: post
title: 全局禁止鼠标右键菜单
---

```
$(document).bind("contextmenu",function(e){
    return false;
});	
$(document).bind("selectstart",function(e){
    return false;
});
```