# prototype

在 ECMAScript 核心所定义的全部属性中，最耐人寻味的就要数 prototype 属性了。对于
ECMAScript 中的引用类型而言， prototype 是保存它们所有实例方法的真正所在。换句话说，诸如
toString() 和 valueOf() 等方法实际上都保存在 prototype 名下，只不过是通过各自对象的实例访
问罢了。在创建自定义引用类型以及实现继承时， prototype 属性的作用是极为重要的。在 ECMAScript 5 中， prototype 属性是不可枚举的，因此使用 for-in 无法发现。

## 使用示例

```javascript

```

## 发布状态

## 浏览器兼容性

## 参考文献

P116