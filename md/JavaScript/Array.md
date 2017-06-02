#  Array

## 属性
属性名 | 描述 
---|---
length          |   返回数组元素数目
constructor     |   返回数组对象引用
prototype       |   为对象添加属性、方法      

## 方法
属性名 | 描述 | 	返回  |   更改原数组
---|---|---|---
concat()	|   连接多个数组                                   |       连接后新数组     |   N
join()     |   将数组中所有元素合为一个字符串。按分隔符划分       |       合并后新数组      |   N
push()	    |   向数组的末尾添加一个/多个元素	                |   新数组长度	            |   Y
pop()	    |   删除数组最后一个元素（栈顶）                  |     删除的元素值            |       Y
shift()     |	删除数组第一个元素	                        |       删除的元素值	        |   Y
unshift()	|   向数组的开头添加一个/多个元素                 |       新数组长度           |       Y
slice(start,end)|	截取从start到end子数组(end省略为数组末尾)    |       截取子数组        |       N
splice()    |	(start,length,item1,item2,…)删除元素并添加新元素  |       删除子数组       |       Y
reverse()	|   颠倒数组中元素的顺序                          |       倒序后数组           |       Y
sort()      |	对数组的元素进行排序(可自定规律,支持传入函数方法)    |       排序后数组       |       Y
toString()  |	数组转换为字符串( 与无参join相同，逗号连接)      |       转换后字符串       |   N
toLocaleString()|	把数组转换为本地字符串                    |       字符串              |       N
valueOf()   |	返回 Array 对象的原始值                         |        Array对象        |       N
isArray()   |   确定传递的值是否为Array  |   |
toSource()	|   返回该对象的源代码。(该特性是非标准的，请尽量不要在生产环境中使用它)   |         |     测试失败
from()

