# contentDocument

这个属性包含一个指针，指向表示框架内容的文档对象。在此之前，无法直接通过元素取得这个文档对象（只能使用 frames 集合）。

## 使用示例

使用这些方法时需要传入表示命名空间的 URI（而不是命名空间前缀），如下面的例子所示。

```javascript
var iframe = document.getElementById("myIframe");
var iframeDoc = iframe.contentDocument; //在 IE8 以前的版本中无效
```

由于 contentDocument 属性是 Document 类型的实例，因此可以像使用其他 HTML 文档一样使
用它，包括所有属性和方法。IE8 之前不支持框架中的 contentDocument 属性，但支持一个名叫 contentWindow 的属性，该属性返回框架的 window 对象，而这个 window 对象又有一个 document 属性。因此，要想在上述所有浏览器中访问内嵌框架的文档对象，可以使用下列代码。

```javascript
var iframe = document.getElementById("myIframe");
var iframeDoc = iframe.contentDocument || iframe.contentWindow.document;
```

所有浏览器都支持 contentWindow 属性。

访问框架或内嵌框架的文档对象要受到跨域安全策略的限制。如果某个框架中的
页面来自其他域或不同子域，或者使用了不同的协议，那么要访问这个框架的文档对
象就会导致错误。

## 发布状态

DOM 2

## 浏览器兼容性

Opera、Firefox、Safari 和 Chrome

## 参考文献

P312