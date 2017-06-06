# OO

### 数据属性

数据属性包含一个数据值的位置。在这个位置可以读取和写入值

- [[Configurable]]：表示能否通过delete 删除属性从而重新定义属性，能否修改属性的特性，或者能否把属性修改为访问器属性。像前面例子中那样直接在对象上定义的属性，它们的这个特性默认值为true。
- [[Enumerable]]：表示能否通过for-in 循环返回属性。像前面例子中那样直接在对象上定义的属性，它们的这个特性默认值为true。
- [[Writable]]：表示能否修改属性的值。像前面例子中那样直接在对象上定义的属性，它们的这个特性默认值为true。
- [[Value]]：包含这个属性的数据值。读取属性值的时候，从这个位置读；写入属性值的时候，把新值保存在这个位置。这个特性的默认值为undefined。

Object.defineProperty() 这个方法接收三个参数：属性所在的对象、属性的名字和一个描述符对象。

描述符（descriptor）对象的属性必须是：configurable、enumerable、writable 和value。

```
var person = {}
Object.defineProperty(person,'name',{
    configurable:false,//能否使用delete、能否需改属性特性、或能否修改访问器属性、，false为不可重新定义，默认值为true
    enumerable:false,//对象属性是否可通过for-in循环，flase为不可循环，默认值为true
    writable:false,//对象属性是否可修改,flase为不可修改，默认值为true
    value:'xiaoming' //对象属性的默认值，默认值为undefined
});

//value
console.log(person);//xiaoming，默认value

//writable
person.name="qiang";
console.log(person);//xiaoming，不可修改value

//enumerable
for(var i in person){
    console.log(person[i]) //无结果，不可循环
}

//configurable
delete person.name
console.log(person.name)//xiaoming，不可删除

Object.defineProperty(person,'name',{
    configurable:true //不可修改，将抛出错误
});
```





