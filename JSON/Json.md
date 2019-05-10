对Json格式的调查
---------------
数据在名称/值对中；
数据由逗号分隔；
花括号保存对象；
方括号保存数组。

Json的书写格式为：名称/值对
-------------------------
名称/值对包括字段名称（在双引号中），后面加一个冒号，然后是值，即：

“firstName”：“John”

等价于下面的JavaScript语句：

firstName=“John”

Json的值
-------
Json的值可以是数字（整数或浮点数）、字符串（在双引号中）、逻辑值（true或false）、数组（在方括号中）、对象（在花括号中）、null。

Json数组
--------
Json数组在方括号中书写：

数组可包含多个对象：
{
“employees”:[
{“firstName”：“John”，“lastName”：“Doe”}，
{“firstName”：“Anna”，“lastName”：“Smith”}，
{“firstName”：“Peter”，“lastName”：“Jones”}
]
}

将景旭师兄给出的示例改写为Json格式
-------------------------------
Layer = 2
Res = 100 10
Thickness = 200
number of source = 1
coordinate of source:
start x | start y | end x | end y
   -50       0       50      0
Amplitude of current = 1
Number of electric dipoles = 10
Number of time = 100
Calculated time range = -5 -2
Number of receiving points = 3
coordinate of receiving points:
|   X   |   Y   |   Z   |
    0      100      0
    0      100     -10
    0      100     -20
File prefix = Model_1
Calculate type = ff

基于Fortran编写信息提取子程序，如下：
------------------------------------