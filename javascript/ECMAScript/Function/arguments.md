# arguments

arguments 是一个类数组对象，包含着传入函数中的所有参数。其实， arguments 对象只是与数组类似（它并不是 Array 的实例），因为可以使用方括号语法访问它的每一个元素（即第一个元素是 arguments[0] ，第二个元素是 argumetns[1] ，以此类推），使用 length 属性来确定传递进来多少个参数。

### 使用示例

```javascript
function sayHi() {
    alert("Hello " + arguments[0] + "," + arguments[1]);
}
```

### 发布状态

### 浏览器兼容性

### 参考文献

P65、P113

---

## arguments.length

通过访问 arguments 对象的 length 属性可以获知有多少个参数传递给了函数。

### 使用示例

```javascript
function howManyArgs() {
    alert(arguments.length);
}
howManyArgs("string", 45); //2
howManyArgs(); //0
howManyArgs(12); //1
```

### 发布状态

### 浏览器兼容性

### 参考文献

P65

---

## arguments.callee

虽然 arguments 的主要用途是保存函数参数，但这个对象还有一个名叫 callee 的属性，该属性是一个指针，指向拥有这个 arguments 对象的函数。

### 使用示例

```javascript
function factorial(num){
    if (num <=1) {
        return 1;
    } else {
        return num * arguments.callee(num-1)
    }
}
```

### 发布状态

### 浏览器兼容性

### 参考文献

P114

---

## arguments.callee.caller

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

---

当函数在严格模式下运行时，访问 arguments.callee 会导致错误。ECMAScript 5 还定义了
arguments.caller 属性，但在严格模式下访问它也会导致错误，而在非严格模式下这个属性始终是
undefined 。定义这个属性是为了分清 arguments.caller 和函数的 caller 属性。以上变化都是为
了加强这门语言的安全性，这样第三方代码就不能在相同的环境里窥视其他代码了。

严格模式还有一个限制：不能为函数的 caller 属性赋值，否则会导致错误。

