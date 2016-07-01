#  scrollIntoView()

通过滚动浏览器窗口或某个容器元素，调用
元素就可以出现在视口中。如果给这个方法传入 true 作为参数，或者不传入任何参数，那么窗口滚动
之后会让调用元素的顶部与视口顶部尽可能平齐。如果传入 false 作为参数，调用元素会尽可能全部
出现在视口中，（可能的话，调用元素的底部会与视口顶部平齐。）不过顶部不一定平齐。

## 使用示例

```javascript
//让元素可见
document.forms[0].scrollIntoView();
```

有了 classList 属性，除非你需要全部删除所有类名，或者完全重写元素的 class 属性，否则也
就用不到 className 属性了。

## 发布状态

HTML5

## 浏览器兼容性

IE、Firefox、Safari 和 Opera

## 参考文献

P298