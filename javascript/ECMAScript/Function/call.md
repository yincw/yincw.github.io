# call()

在特定的作用域中调用函数，实际上等于设置函数体内 this 对象的值。相对与 apply() 方法，对于 call()
方法而言，第一个参数是 this 值没有变化，变化的是其余参数都直接传递给函数。换句话说，在使用
call() 方法时，传递给函数的参数必须逐个列举出来。

## 使用示例

```javascript
function sum(num1, num2){
    return num1 + num2;
}

function callSum(num1, num2){
    return sum.call(this, num1, num2);
}

alert(callSum(10,10)); //20
```

## 发布状态

## 浏览器兼容性

## 参考文献

P117