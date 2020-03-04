---
layout: post
title: CSS Circle
---

```HTML
<div class="circle"></div>
```

```CSS
.circle {
  border-radius: 50%;
  width: 2rem;
  height: 2rem;
  background: #333;
}
```

## Explanation
- border-radius: 50% curves the borders of an element to create a circle.
- Since a circle has the same radius at any given point, the width and height must be the same. Differing values will create an ellipse.