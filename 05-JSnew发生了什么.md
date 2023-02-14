## 05-JSnew发生了什么
> new是面向对象编程OOP的编程范式的一个关键词

+ es6的继承
```javascript
  class Person {
    constructor(name) {
      this.name = name;
    }
    say() {
      console.log(`My Name is ${this.name}`);
    }
  }

  const p = new Person('gouwa');
  p.say();
```
+ es5
```javascript
  function Person(name) {
    this.name = name;
  }
  Person.prototype.say = () => {
    console.log(`My Name is ${this.name}`);
  }
  const p = new Person('gouwa');
  p.say();
```
+ 实现new
```javascript
  const myNew = (fn, ...args) => {
    // 产生新对象
    const obj = {};
    // 修改新对象原型链
    obj.__proto__ = fn.prototype;
    // 执行构造函数 将构造函数的this指向新对象
    const res = fn.apply(obj, args)
    // 返回新对象
    return typeof res === 'object' ? res : obj;
  }
```