---
layout: post
title: Cookie
---

##### 解决办法，就是在iframe加载完成后，设置 iframe里面body的宽度为多少PX。


```
$("#iframe1")[0].onload = function () {
    iosIframeWidthBug();
}
```

```
/*修复ios iframe width bug*/
function iosIframeWidthBug(){
    //不是 iphone ipad就不执行了
    if (!navigator.userAgent.match(/iPad|iPhone/i)){
        return false;
    }else{
        //获取子iframe
        var iframebody = document.getElementById('iframe1').contentWindow.document.body;
        iframebody.style.width = document.body.clientWidth+'px';
    }
}
```
