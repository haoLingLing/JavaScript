# 你不知道的JavaScript 中
## 原生函数
常用的原生函数有
- string
- Number
- Boolean
- Array
- Object
- Function
- RegExp
- Date
- Error
- Symbol

基础类型的可以使用toString方法
```javascript
string -> string
number -> '1'
true -> "true"
[1,2,3]-> "1,2,3"
[{firstName:'bolo'}] -> [object Object]
Symbol(1) -> "Symbol(1)"
```

内部属性[[class]]
所有的typeOOf 返回值为Object 对象都包含一个内部属性[[class]]，属性无法直接访问，可以通过Object.prototype.call()
```js
Object.prototype.call([1,2,3]) //  [object Array]
Object.prototype.call({firstName:'bolo'}) //  [object Object]
Object.prototype.call(/regex-literal/i) //  [object RegExp]
Object.prototype.call(null) //  [object Null]
Object.prototype.call(undefined) //  [object Undefined]

Object.prototype.call("abc") //  [object String]
Object.prototype.call(true) //  [object Boolean]
Object.prototype.call(42) //  [object Number]
```