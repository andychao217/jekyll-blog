---
layout: post
title: jQuery将表单序列化成一个Object对象的实例
---

```javascript
(function($){ 
  $.fn.extend({ 
    serializeObject:function(){ 
      if(this.length>1){ 
        return false; 
      } 
      var arr=this.serializeArray(); 
      var obj=new Object; 
      $.each(arr,function(k,v){ 
        obj[v.name]=v.value; 
      }); 
      return obj; 
    } 
  }); 
})(jQuery); 

$(":button").click(function(){
       var test=$("form").serializeObject();
       alert(test.id);     
    });
```


```HTML
<body>
    <form action="" method="get">
        <input name="id" type="hidden" value="110" />
        <input name="test" type="text" />
        <input name="" type="button" />
    </form>
</body>
```

