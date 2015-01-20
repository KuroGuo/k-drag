## K-drag

### Quick Examples

```html
<style>
  #box {
    position: absolute;
    width: 60px;
    height: 60px;
    background-color: #369;
  }
</style>
<script src='k-drag.js'></script>
<div id="box"></div>
```

```javascript
var box = document.querySelector('#box');

kDrag.bind(box);

var x, y;

box.addEventListener('k.dragstart', function () {
  console.log('dragstart');
});

box.addEventListener('k.drag', function (e) {
  x += e.stepX;
  y += e.stepY;

  box.style.left = x + 'px';
  box.style.top = y + 'px';
});

box.addEventListener('k.dragend', function () {
  console.log('dragend');
});
```