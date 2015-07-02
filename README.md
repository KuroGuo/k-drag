## K-Drag

High performance drag component.

### Install

```bash
$ npm install k-drag
```

### Quick Example

<a href="http://kuroguo.github.io/k-drag/example/" target="_blank">example</a>

```html
<style>
  #box {
    position: absolute;
    width: 60px;
    height: 60px;
    background-color: #369;
  }
</style>
<div id="box"></div>
<script src='k-drag.js'></script>
<script>
  var box = document.querySelector('#box')

  kDrag.bind(box)

  var x = 0, y = 0

  box.addEventListener('k.dragstart', function () {
    console.log('dragstart')
  })

  box.addEventListener('k.drag', function (e) {
    x += e.stepX
    y += e.stepY

    box.style.left = x + 'px'
    box.style.top = y + 'px'
  })

  box.addEventListener('k.dragend', function () {
    console.log('dragend')
  })
</script>
```

### Events

* k.dragstart
* k.drag
* k.dragSync(sync version of k.drag, k.drag is a async event)
* k.dragend
