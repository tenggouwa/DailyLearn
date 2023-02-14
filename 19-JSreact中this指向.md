## react中this指向

+ 在react class中不绑定this 
  + 函数中的this指向的是react中的context 而不是当前实例中的this
  + 所以需要手动绑定bind或者使用箭头函数