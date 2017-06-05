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

- callee













