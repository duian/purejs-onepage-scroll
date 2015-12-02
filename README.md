移动端单页滚动脚本
=======================
原来的onepage-scroll中的自定义的'swipeLeft'事件的方式部分机型不兼容。改写了自定义事件的方式。
```js
var event = new Event('swipeLeft');
document.dispatchEvent(event);
```
改为
```js
var event = document.createEvent('HTMLEvents');
event.initEvent('swipeLeft', true, true);
event.eventType = 'message';
document.dispatchEvent(event);
```

基于[One Page Scroll](https://github.com/peachananr/onepage-scroll)
