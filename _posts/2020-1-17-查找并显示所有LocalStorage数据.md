---
layout: post
title: Cookie
---

```
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
