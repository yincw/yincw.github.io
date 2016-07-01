# innerWidth()

`窗口大小`



## 使用示例

```javascript
```

在 IE9+、Safari和 Firefox 中， outerWidth 和 outerHeight 返回浏览器窗口本身的尺寸（无论是从最外层的 window 对象还是从某个框架访问）。在Opera中，这两个属性的值表示页面视图容器① 的大小。而 innerWidth 和 innerHeight
则表示该容器中页面视图区的大小（减去边框宽度）。在 Chrome 中， outerWidth 、 outerHeight 与 innerWidth 、 innerHeight 返回相同的值，即视口（viewport）大小而非浏览器窗口大小。

IE8 及更早版本没有提供取得当前浏览器窗口尺寸的属性；不过，它通过 DOM 提供了页面可见区域
的相关信息。

在 IE、Firefox、Safari、Opera 和 Chrome 中， document.documentElement.clientWidth 和
document.documentElement.clientHeight 中保存了页面视口的信息。在 IE6 中，这些属性必须在
标准模式下才有效；如果是混杂模式，就必须通过 document.body.clientWidth 和 document.body.
clientHeight 取得相同信息。而对于混杂模式下的 Chrome，则无论通过 document.documentEle-
ment 还是 document.body 中的 clientWidth 和 clientHeight 属性，都可以取得视口的大小。

## 发布状态

## 浏览器兼容性

IE9+、Firefox、Safari、Opera 和 Chrome

## 参考文献

P198