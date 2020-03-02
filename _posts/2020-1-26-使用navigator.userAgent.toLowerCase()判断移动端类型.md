---
layout: post
title: Cookie
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