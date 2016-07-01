# apply()

在特定的作用域中调用函数，实际上等于设置函数体内 this 对象的值。接收两个参数：一个是在其中运行函数的作用域，另一个是参数数组。其中，第二个参数可以是 Array 的实例，也可以是 arguments 对象。

## 使用示例

```javascript
function sum(num1, num2){
    return num1 + num2;
}

function callSum1(num1, num2){
    return sum.apply(this, arguments); // 传入 arguments 对象
}

function callSum2(num1, num2){
    return sum.apply(this, [num1, num2]); // 传入数组
}

alert(callSum1(10,10)); //20
alert(callSum2(10,10)); //20
```

在严格模式下，未指定环境对象而调用函数，则 this 值不会转型为 window 。
除非明确把函数添加到某个对象或者调用 apply() 或 call() ，否则 this 值将是
undefined 。

事实上，传递参数并非 apply() 和 call() 真正的用武之地；它们真正强大的地方是能够扩充函数
赖以运行的作用域。

```javascript
window.color = "red";
var o = { color: "blue" };

function sayColor(){
    alert(this.color);
}

sayColor(); //red

sayColor.call(this); //red
sayColor.call(window); //red
sayColor.call(o); //blue
```

## 发布状态

## 浏览器兼容性

## 参考文献

P116