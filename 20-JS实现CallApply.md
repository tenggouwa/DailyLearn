## 实现CallApply

```js
  function myCall (context, ...args) {
    // this指向的是被执行的方法
    context.fn = this;
    const res = context.fn(...args);
    delete context.fn;
    return res;
  }

  function myApply(context, args) {
    context.fn = this;
    const res = context.fn(...args);
    delete context.fn;
    return res;

  }

  function bind(context, args) {
    context.fn = this;
    return function () {
      return fn.myApply(context, [...args, ...arguments])
    };
  }
```