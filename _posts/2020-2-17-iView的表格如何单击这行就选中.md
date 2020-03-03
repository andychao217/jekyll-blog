---
layout: post
title: iView的表格如何单击这行就选中
---

```
<Table 
    border 
    ref="table" 
    :columns="columns" 
    :data="list" 
    @on-row-click="rowClick" 
    @on-selection-change="SelectGoods"
>
</Table>

rowClick(data,index){
    this.$refs.table.toggleSelect(index);
}
```
