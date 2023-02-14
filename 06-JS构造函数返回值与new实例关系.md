## JS构造函数返回值与new实例关系

如果返回{},null, 1, true 应该怎么返回？

+ 对于基本数据类型来说， new返回的是空对象
+ 对于引用数据类型 返回的是 构造函数的返回值

```javascript
  console.table(
    [null, undefined, 1, true, Symbol(), {}, [1, 2]]
    .map(v => [v, function() {return v}])
    .map(([ret, myConstructor]) => [Object.prototype.toString.call(ret), ret, new myConstructor()])
  )
```