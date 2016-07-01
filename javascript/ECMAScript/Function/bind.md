# bind()

创建一个函数的实例，其 this 值会被绑定到传给 bind() 函数的值。

## 使用示例

```javascript
window.color = "red";
var o = { color: "blue" };

function sayColor(){
    alert(this.color);
}

var objectSayColor = sayColor.bind(o);
objectSayColor(); //blue
```

## 发布状态

ECMAScript 5

## 浏览器兼容性

IE9+、Firefox 4+、Safari 5.1+、Opera 12+和 Chrome

## 参考文献

P117