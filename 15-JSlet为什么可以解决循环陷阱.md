## let为什么可以解决循环陷阱

```js
var a = [];
for (var i = 0; i < 10; i++) {
  a[i] = function () {
    console.log(i);
  };
}
a[6]()
// 1.立即执行函数
// 2.let声明i
```