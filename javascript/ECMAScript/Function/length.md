# length

表示函数希望接收的命名参数的个数。

## 使用示例

```javascript
function sayName(name){
    alert(name);
}

function sum(num1, num2){
    return num1 + num2;
}

function sayHi(){
    alert("hi");
}

alert(sayName.length); //1
alert(sum.length); //2
alert(sayHi.length); //0
```

## 发布状态

## 浏览器兼容性

## 参考文献

P116