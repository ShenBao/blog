#  Date

## 属性
属性名 | 描述 
---|---
constructor	    |   返回对创建此对象的 Date 函数的引用。
prototype	    |   添加属性和方法

## 方法
方法  |   描述
---|---
Date()	        |   返回当日的日期和时间。
parse()         |   返回1970年1月1日午夜到指定日期（字符串）的毫秒数。
UTC()           |   根据世界时返回 1970 年 1 月 1 日 到指定日期的毫秒数。
now() <sup>es5</sup>  |   返回表示调用这个方法时的日期和时间的毫秒数.
getDate()       |   从 Date 对象返回一个月中的某一天 (1 ~ 31)。
getDay()        |   从 Date 对象返回一周中的某一天 (0 ~ 6)。
getMonth()      |   从 Date 对象返回月份 (0 ~ 11)。
getFullYear()   |   从 Date 对象以四位数字返回年份。
getYear() <sup>废弃</sup>  |   请使用 getFullYear() 方法代替。
getHours()      |   返回 Date 对象的小时 (0 ~ 23)。
getMinutes()    |   返回 Date 对象的分钟 (0 ~ 59)。
getSeconds()    |   返回 Date 对象的秒数 (0 ~ 59)。
getMilliseconds()|	返回 Date 对象的毫秒(0 ~ 999)。
getTime()       |   返回 1970 年 1 月 1 日至今的毫秒数。
getTimezoneOffset()     |   返回本地时间与格林威治标准时间 (GMT) 的分钟差。
getUTCDate()            |   根据世界时从 Date 对象返回月中的一天 (1 ~ 31)。
getUTCDay()             |   根据世界时从 Date 对象返回周中的一天 (0 ~ 6)。
getUTCMonth()           |   根据世界时从 Date 对象返回月份 (0 ~ 11)。
getUTCFullYear()        |   根据世界时从 Date 对象返回四位数的年份。
getUTCHours()           |   根据世界时返回 Date 对象的小时 (0 ~ 23)。
getUTCMinutes()         |   根据世界时返回 Date 对象的分钟 (0 ~ 59)。
getUTCSeconds()         |   根据世界时返回 Date 对象的秒钟 (0 ~ 59)。
getUTCMilliseconds()    |   根据世界时返回 Date 对象的毫秒(0 ~ 999)。
setDate()       |   设置 Date 对象中月的某一天 (1 ~ 31)。
setMonth()      |   设置 Date 对象中月份 (0 ~ 11)。
setFullYear()   |   设置 Date 对象中的年份（四位数字）。
setYear()<sup>废弃</sup>  |   请使用 setFullYear() 方法代替。
setHours()      |   设置 Date 对象中的小时 (0 ~ 23)。
setMinutes()    |   设置 Date 对象中的分钟 (0 ~ 59)。
setSeconds()    |   设置 Date 对象中的秒钟 (0 ~ 59)。
setMilliseconds()|  设置 Date 对象中的毫秒 (0 ~ 999)。
setTime()       |   以毫秒设置 Date 对象。
setUTCDate()    |   根据世界时设置 Date 对象中月份的一天 (1 ~ 31)。
setUTCMonth()   |   根据世界时设置 Date 对象中的月份 (0 ~ 11)。
setUTCFullYear()|   根据世界时设置 Date 对象中的年份（四位数字）。
setUTCHours()   |   根据世界时设置 Date 对象中的小时 (0 ~ 23)。
setUTCMinutes() |   根据世界时设置 Date 对象中的分钟 (0 ~ 59)。
setUTCSeconds() |   根据世界时设置 Date 对象中的秒钟 (0 ~ 59)。
setUTCMilliseconds()|   根据世界时设置 Date 对象中的毫秒 (0 ~ 999)。
toSource()      |   返回该对象的源代码。
toDateString()  |   把 Date 对象的日期部分转换为字符串,以特定于实现的格式显示星期几、月、日和年；
toTimeString()  |   把 Date 对象的时间部分转换为字符串,以特定于实现的格式显示时、分、秒和时区；
toLocaleDateString() |   根据本地时间格式，把 Date 对象的日期部分转换为字符串,以特定于地区的格式显示星期几、月、日和年；
toLocaleTimeString() |   根据本地时间格式，把 Date 对象的时间部分转换为字符串,以特定于实现的格式显示时、分、秒；
toLocaleString()|   根据本地时间格式，把 Date 对象转换为字符串。
toUTCString()   |   根据世界时，把 Date 对象转换为字符串。
toGMTString()<sup>废弃</sup>   |   请使用 toUTCString() 方法代替。
toString()      |   把 Date 对象转换为字符串，返回带有时区信息的日期和时间，其中时间一般以军用时间（即小时的范围是0 到23）表示
valueOf()           |   不返回字符串，而是返回日期的毫秒表示


## 创建对象

```
var myDate = new Date();//初始值为系统当前时间
//英文表示月份名称，从January到December
new Date("July 22,1994 12:15:00");//
new Date("July 22,1994"); 
//整数表示月份，从0到11 
new Date(1994,6,22,12,15,00); 
new Date(1994,6,22); 
new Date(1137075575000); //参数表示的是需要创建的时间和 GMT时间1970年1月1日之间相差的毫秒数
```
这里有个小问题：为什么时间初始是从1970年1月1日0点开始呐？

很多编程语言起源于UNIX系统，而1970年1月1日0点算 UNIX 和 C语言 生日(贝尔实验室)。最初计算机操作系统是32位，而时间也是用32位表示，能表示的最长时间范围为68年，超出时间范围会发生时间回归的现象。

## 方法使用

Date() 返回当前系统时间
```
console.log(Date()); //Fri Mar 24 2017 21:15:09 GMT+0800 (中国标准时间)
```

getDate() 返回日期
```
var birthday = new Date("July 22, 1994 12:15:00");
console.log(birthday.getDate()); //22
```

getTime()返回距离1970 年 1 月 1 日的毫秒数
```
var d = new Date(); 
var a = new Date("July 22,1994");
console.log(d.getTime() + "        " + a.getTime()); //1490363547304        774806400000
```

getTimezoneOffset() 本地时间与 GMT 时间之间的时间差，以分钟为单位

返回之所以以分钟计，而不是以小时计，原因是某些国家所占有的时区甚至不到一个小时的间隔
```
var d = new Date();
var gmtHours = d.getTimezoneOffset()/60;
console.log("The local time zone is: GMT " + gmtHours); //The local time zone is: GMT -8
```
