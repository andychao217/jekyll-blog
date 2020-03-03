---
layout: post
title: iView的表格如何单击这行就选中
---

```HTML
<Table 
    border 
    ref="table" 
    :columns="columns" 
    :data="list" 
    @on-row-click="rowClick" 
    @on-selection-change="SelectGoods"
>
</Table>
```
```javascript
rowClick(data,index){
    this.$refs.table.toggleSelect(index);
}
```
