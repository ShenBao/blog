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













