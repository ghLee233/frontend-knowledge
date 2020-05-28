- 对象上有 `__proto__` 属性，称之为原型， `__proro__`指向的对象，称之为原型对象

- 函数上有`prototype`属性, `prototype`也是一个对象，有自己的`__proto__` 

- `new` 一个新对象时，新对象的 `__proto__` 指向函数的 `prototype`，构成原型链

- 也可以使用 `Object.create`或者`Object.setPrototypeOf`显示设置

  

  

