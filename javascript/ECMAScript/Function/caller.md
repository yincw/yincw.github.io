# caller

这个属性中保存着调用当前函数的函数的引用，如果是在全局作用域中调用当前函数，它的值为 null 。

## 使用示例

```javascript
function outer(){
    inner();
}

function inner(){
    alert(arguments.callee.caller);
}

outer();
```

## 发布状态

ECMAScript 5

## 浏览器兼容性

IE、Firefox、Chrome 和 Safari 的所有版本以及 Opera 9.6

## 参考文献

P115