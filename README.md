# Rem.js
v0.0.1
## js
```js
<script>
(function (doc, win) {
  var docEl = doc.documentElement;
  var resizeEvt = 'orientationchange' in window ? 'orientationchange' : 'resize';
  var recalc = function () {
    var clientWidth = docEl.clientWidth;
    if (!clientWidth) return;
    //     加 130px 的限制
    docEl.style.fontSize = ((100 * (clientWidth / 375)) > 130 ? 130 : (100 * (clientWidth / 375))) + 'px';
  };

    if (!doc.addEventListener) return;
    win.addEventListener(resizeEvt, recalc, false);
    doc.addEventListener('DOMContentLoaded', recalc, false);
})(document, window);
</script>
```
## CSS 
```css
html{
  font-size: 100px;
}
body{
  font-size: .14rem;
}
```
