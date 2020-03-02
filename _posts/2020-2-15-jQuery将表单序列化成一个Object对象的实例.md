---
layout: post
title: Cookie
---

```
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


```
<body>
    <form action="" method="get">
        <input name="id" type="hidden" value="110" />
        <input name="test" type="text" />
        <input name="" type="button" />
    </form>
</body>
```

