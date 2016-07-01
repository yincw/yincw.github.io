# document.defaultView

其中保存着一个指针，指向拥有给定文档的窗口（或框架）。除此之外，“视图”规范没有提供什么时候其他视图可用的信息，因而这是唯一一个新增的属性。除 IE 之外的所有浏览器都支持 defaultView 属性。在 IE 中有一个等价的属性名叫 parentWindow （Opera 也支持这个属性）。因此，要确定文档的归属窗口，可以使用以下代码。

## 使用示例

```javascript
var parentWindow = document.defaultView || document.parentWindow;
```

## 发布状态

DOM2 级视图

## 浏览器兼容性

## 参考文献

P310