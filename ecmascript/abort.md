# abort()

用于停止正在进行的请求。

## 使用示例

```javascript
xhr.abort();
```

调用这个方法后， XHR 对象会停止触发事件，而且也不再允许访问任何与响应有关的对象属性。在
终止请求之后，还应该对 XHR 对象进行解引用操作。由于内存原因，不建议重用 XHR 对象。

## 发布状态

## 浏览器兼容性

## 参考文献

P575