# this

函数内部的另一个特殊对象是 this ，其行为与 Java 和 C#中的 this 大致类似。换句话说， this
引用的是函数据以执行的环境对象——或者也可以说是 this 值（当在网页的全局作用域中调用函数时， this 对象引用的就是 window ）。

## 使用示例

```javascript
window.color = "red";
var o = { color: "blue" };

function sayColor(){
    alert(this.color);
}

sayColor(); //"red"

o.sayColor = sayColor;
o.sayColor(); //"blue"
```

## 发布状态

## 浏览器兼容性

## 参考文献

P114
