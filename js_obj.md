js
#### 获取对象原形的通用方法
`
console.log(Object.getPrototypeOf(a))
`
#### js判断对象类型的通用方法
`
console.log(Object.prototype.toString.call(a))
`
但需要注意的是，call 本身会产生装箱操作，所以需要配合 typeof 来区分基本类型还是对象类型。拆箱转换

#### js new构造函数内部做了什么

1. 创建一个空对象 var obj = {}
2. 将空对象的原形设置为构造函数的原形   Object.setProperty(obj,this.constructor.property)
3. 调用构造函数 this.constructor.call(obj)
4. 返回这个对象

1.以构造器的 prototype 属性（注意与私有字段[[prototype]]的区分）为原型，创建新对象；
2.将 this 和调用参数传给构造器，执行；
3.如果构造器返回的是对象，则返回，否则返回第一步创建的对象。

#### js 构造函数中有返回值会怎样，返回对象会怎样

1. 如果构造函数中返回的是对象，则创建的实例为返回的对象，否则为自身。

### 为什么typeof null === Object

typeof null结果是object, 这是个历史遗留bug
https://www.zhihu.com/question/21691758

