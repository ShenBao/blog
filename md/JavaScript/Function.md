# Function

### 函数声明与函数表达式

```
function fn(){
    //doSomething
}

var fn = function(){
    //doSomething
}

var fn = new Function("参数1", "参数2", "函数体doSomething"); // 不推荐
```

函数没有重载,后面的函数覆盖了前面的函数；

### 函数内部属性

有两个特殊的对象：arguments 和this

- callee ： 当函数被调用时，它的arguments.callee对象就会指向自身，也就是一个对自己的引用。由于arguments在函数被调用时才有效，因此arguments.callee在函数未调用时是不存在的（即null.callee），且解引用它会产生异常。
- caller ： 在一个函数调用另一个函数时，被调用函数会自动生成一个caller属性，指向调用它的函数对象。如果该函数当前未被调用，或并非被其他函数调用，则caller为null。

## 函数属性和方法

每个函数都包含两个属性：length 和prototype。

- length 属性表示函数希望接收的命名参数的个数

- prototype 是保存它们所有实例方法的真正所；ECMAScript 5 中，prototype 属性是不可枚举的，因此使用for-in 无法发现。

每个函数都包含两个非继承而来的方法：apply()和call()；这两个方法的用途都是在特定的作用域中调用函数，实际上等于设置函数体内this 对象的值。

- apply()方法接收两个参数：一个是在其中运行函数的作用域，另一个是参数数组。其中，第二个参数可以是Array 的实例，也可以是arguments 对象。
- call()方法与apply()方法的作用相同，它们的区别仅在于接收参数的方式不同。对于call()方法而言，第一个参数是this 值没有变化，变化的是其余参数都直接传递给函数。换句话说，在使用call()方法时，传递给函数的参数必须逐个列举出来
- bind()

## 继承方法

- toLocaleString()
- toString()






