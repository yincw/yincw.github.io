# DOMMouseScroll

在鼠标滚轮滚动时触发。与 mousewheel 事件一样， DOMMouseScroll 也被视为鼠标事件，因而包含与鼠标事件有关的所有属性。而有关鼠标滚
轮的信息则保存在 detail 属性中，当向前滚动鼠标滚轮时，这个属性的值是 -3 的倍数，当向后滚动
鼠标滚轮时，这个属性的值是 3 的倍数。

支持属性：

* event.detail

## 使用示例

```javascript
EventUtil.addHandler(window, "DOMMouseScroll", function(event){
    event = EventUtil.getEvent(event);
    alert(event.detail);
});
```

## 发布状态

## 浏览器兼容性

Firefox

## 参考文献

P377