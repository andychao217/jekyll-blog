---
layout: post
title: 使用Navigator.userAgent.toLowerCase()判断移动端类型
---

```javascript
var ua = navigator.userAgent.toLowerCase();
if (/android|adr/gi.test(ua)) {
    // 安卓
     
}else if(/\(i[^;]+;( U;)? CPU.+Mac OS X/gi.test(ua)){
    //苹果
     
}else if(/iPad/gi.test(ua)){
    //ipad

}