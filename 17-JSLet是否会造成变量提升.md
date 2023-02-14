## JSLet是否会造成变量提升
> 函数也有变量提升

+ let会出现暂时性死区 
  + 也会变量提升 但和var的区别在于 没有复制为undefined而是报错
```js
var a = 8;
(
  function(){
    console.log(a); // 报错
    let a = 1;
  }
)();
```