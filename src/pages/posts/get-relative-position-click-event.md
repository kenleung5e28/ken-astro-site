---
title: "Get mouse position relative to click event target"
date: "2020-11-20"
draft: false
tags:
- javascript
---

```js
document.getElementById('clickme').onclick = function clickEvent(e) {
  // e = Mouse click event.
  var rect = e.target.getBoundingClientRect();
  var x = e.clientX - rect.left; // x position within the element.
  var y = e.clientY - rect.top;  // y position within the element.
  console.log("Left? : " + x + " ; Top? : " + y + ".");
}
```