#   Location 

Location 对象包含有关当前 URL 的信息。

Location 对象是 Window 对象的一个部分，可通过 window.location 属性来访问。

##  Location 对象属性
属性	|   描述
---|---
hash	|   设置或返回从井号 (#) 开始的 URL（锚）。
host	|   设置或返回主机名和当前 URL 的端口号。
hostname|   设置或返回当前 URL 的主机名。
href	|   设置或返回完整的 URL。
pathname|   设置或返回当前 URL 的路径部分。
port	|   设置或返回当前 URL 的端口号。
protocol|	设置或返回当前 URL 的协议。
search	|   设置或返回从问号 (?) 开始的 URL（查询部分）。


##  Location 对象方法
属性	|   描述
---|---
assign()	|   加载新的文档。
reload()	|   重新加载当前文档。
replace()	|   用新的文档替换当前文档。