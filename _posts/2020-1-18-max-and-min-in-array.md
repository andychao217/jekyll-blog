---
layout: post
title: 数组比最大值和最小值
---

```javascript
Array.prototype.max = function() {
	return Math.max.apply({},this)

}
Array.prototype.min = function() {
	return Math.min.apply({},this)
}

array.min()

array.max()
```
