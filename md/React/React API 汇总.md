
# React Top-Level API 汇总


ES6
```
import React from 'react'
```

ES5
```
var React = require('react')
```

## React

ES6
```
React.Component
React.PureComponent
```
ES5
```
createClass()
```

## Creating React Elements

```
createElement()
createFactory()
```

## Transforming Elements API

```
cloneElement()
isValidElement()
React.Children
```


# 参考用法

## React.Component
```
class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

## React.PureComponent
```
用法同上，多了shouldComponentUpdate()
```

## createClass()
```
React.createClass(specification)
即：
var Greeting = React.createClass({
  render: function() {
    return <h1>Hello, {this.props.name}</h1>;
  }
});
```

## createElement()
```
React.createElement(
  type,
  [props],
  [...children]
)
```

## cloneElement()
```
React.cloneElement(
  element,
  [props],
  [...children]
)
废弃了 React.addons.cloneWithProps()
```

## createFactory()
```
React.createFactory(type)
```

## isValidElement()
```
React.isValidElement(object)
返回true或false
```

## React.Children
```
React.Children: object
```

### React.Children.map
```
React.Children.map(children, function[(thisArg)])
```

### React.Children.forEach
```
React.Children.forEach(children, function[(thisArg)])
```

### React.Children.count
```
React.Children.count(children)
```

### React.Children.only
```
React.Children.only(children)
```

### React.Children.toArray
```
React.Children.toArray(children)
```


## React.PropTypes

```
MyComponent.propTypes = {
  // 可以声明 prop 为指定的 JS 基本类型。默认
  // 情况下，这些 prop 都是可传可不传的。
  optionalArray: React.PropTypes.array,
  optionalBool: React.PropTypes.bool,
  optionalFunc: React.PropTypes.func,
  optionalNumber: React.PropTypes.number,
  optionalObject: React.PropTypes.object,
  optionalString: React.PropTypes.string,
  optionalSymbol: React.PropTypes.symbol,

  // 所有可以被渲染的对象：数字，
  // 字符串，DOM 元素或包含这些类型的数组。
  optionalNode: React.PropTypes.node,

  // React 元素
  optionalElement: React.PropTypes.element,

  // 用 JS 的 instanceof 操作符声明 prop 为类的实例。
  optionalMessage: React.PropTypes.instanceOf(Message),

  // 用 enum 来限制 prop 只接受指定的值。
  optionalEnum: React.PropTypes.oneOf(['News', 'Photos']),

  // 指定的多个对象类型中的一个
  optionalUnion: React.PropTypes.oneOfType([
    React.PropTypes.string,
    React.PropTypes.number,
    React.PropTypes.instanceOf(Message)
  ]),

  // 指定类型组成的数组
  optionalArrayOf: React.PropTypes.arrayOf(React.PropTypes.number),

  // 指定类型的属性构成的对象
  optionalObjectOf: React.PropTypes.objectOf(React.PropTypes.number),

  // 指定Object对象内各属性的类型
  optionalObjectWithShape: React.PropTypes.shape({
    color: React.PropTypes.string,
    fontSize: React.PropTypes.number
  }),

  // 加上 `isRequired` 来要求该 prop 不可为空
  requiredFunc: React.PropTypes.func.isRequired,

  // 不可为空的任意类型
  requiredAny: React.PropTypes.any.isRequired,

  // 自定义验证器。如果验证失败需要返回一个 Error 对象。不要直接
  // 使用 `console.warn` 或抛异常，因为这样 `oneOfType` 会失效。
  customProp: function(props, propName, componentName) {
    if (!/matchme/.test(props[propName])) {
      return new Error(
        'Invalid prop `' + propName + '` supplied to' +
        ' `' + componentName + '`. Validation failed.'
      );
    }
  },

  // You can also supply a custom validator to `arrayOf` and `objectOf`.
  // It should return an Error object if the validation fails. The validator
  // will be called for each key in the array or object. The first two
  // arguments of the validator are the array or object itself, and the
  // current item's key.
  customArrayProp: React.PropTypes.arrayOf(function(propValue, key, componentName, location, propFullName) {
    if (!/matchme/.test(propValue[key])) {
      return new Error(
        'Invalid prop `' + propFullName + '` supplied to' +
        ' `' + componentName + '`. Validation failed.'
      );
    }
  })
};
```

### 示例

```
class MyComponent extends React.Component {
  render() {
    // This must be exactly one element or it will warn.
    const children = this.props.children;
    return (
      <div>
        {children}
      </div>
    );
  }
}

MyComponent.propTypes = {
  children: React.PropTypes.element.isRequired
};
```

## React.addons
```

```
























