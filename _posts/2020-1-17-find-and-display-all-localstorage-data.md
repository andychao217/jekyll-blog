---
layout: post
title: 查找并显示所有LocalStorage数据
---

```javascript
function findAllLocalStorageItems(){
    var itemList = document.getElementById('itemlist');
    
    itemList.innerHTML = '';
    
    for(var i = 0; i<localStorage.length; i++){
        var key = localStorage.key(i);
        
        var item = localStorage.getItem(key);
        
        var newItem = document.createElement('li');
        newItem.innerHTML = key + ": " + item;
        itemList.appendChild(newItem);
    }
}
```
