# event.data

其中包含以下几个值中的一个：

* 如果在 compositionstart 事件发生时访问，包含正在编辑的文本（例如，已经选中的需要马上替换的文本）；
* 如果在 compositionupdate 事件发生时访问，包含正插入的新字符；
* 如果在 compositionend 事件发生时访问，包含此次输入会话中插入的所有字符。

## 使用示例

```javascript
var textbox = document.getElementById("myText");
EventUtil.addHandler(textbox, "compositionstart", function(event){
    event = EventUtil.getEvent(event);
    alert(event.data);
});
EventUtil.addHandler(textbox, "compositionupdate", function(event){
    event = EventUtil.getEvent(event);
alert(event.data);
});
EventUtil.addHandler(textbox, "compositionend", function(event){
    event = EventUtil.getEvent(event);
    alert(event.data);
});
```

## 发布状态

## 浏览器兼容性

IE 9+

## 参考文献

P385