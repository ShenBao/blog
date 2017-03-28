# Navigator
Navigator 对象包含有关浏览器的信息。


## Navigator 对象集合
集合	|   描述
---|---
plugins[]	|   返回对文档中所有嵌入式对象的引用。<br/>该集合是一个 Plugin 对象的数组，其中的元素代表浏览器已经安装的插件。Plug-in 对象提供的是有关插件的信息，其中包括它所支持的 MIME 类型的列表。<br/>虽然 plugins[] 数组是由 IE 4 定义的，但是在 IE 4 中它却总是空的，因为 IE 4 不支持插件和 Plugin 对象。


##  Navigator 对象属性
属性	|   描述
---|---
appCodeName	    |   返回浏览器的代码名。
appMinorVersion	|   返回浏览器的次级版本。
appName	        |   返回浏览器的名称。
appVersion	    |   返回浏览器的平台和版本信息。
browserLanguage	|   返回当前浏览器的语言。
cookieEnabled	|   返回指明浏览器中是否启用 cookie 的布尔值。
cpuClass	    |   返回浏览器系统的 CPU 等级。
onLine	        |   返回指明系统是否处于脱机模式的布尔值。
platform	    |   返回运行浏览器的操作系统平台。
systemLanguage	|   返回 OS 使用的默认语言。
userAgent	    |   返回由客户机发送服务器的 user-agent 头部的值。
userLanguage	|   返回 OS 的自然语言设置。



##  Navigator 对象方法
方法	|   描述
---|---
javaEnabled()	|   规定浏览器是否启用 Java。
taintEnabled()	|   规定浏览器是否启用数据污点 (data tainting)。








