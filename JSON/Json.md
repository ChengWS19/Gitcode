对Json格式的调查
---------------
首先提出问题，为什么要采用Json格式即研究的必要性。



结论：之所以要采用Json这种数据交换格式是因为对于软件的开发需要更加规范的数据格式，并且适用于多种语言，这样才可以更好的进行统一解析。

Json中一共只有以下几种数据类型：
------------------------------
·number：数字（整数或浮点数）
·boolean：逻辑判断（true或false）
·string："字符串"（在双引号中）
·null：零值
·array：[数组]（在方括号中）
·object：{对象}(在花括号中)

Json的书写格式为：名称/值对
-------------------------
名称/值对包括字段名称（在双引号中），后面加一个冒号，然后是值，即：
“firstName”：“John”
等价于下面的JavaScript语句：
firstName=“John”

Json数组
--------
Json数组可包含多个对象：
{
“employees”:[
{“firstName”：“John”，“lastName”：“Doe”}，
{“firstName”：“Anna”，“lastName”：“Smith”}，
{“firstName”：“Peter”，“lastName”：“Jones”}
]
}

根据上述规则将景旭师兄给出的示例改写为Json格式
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

Json格式
---------
{"layer":"2",
"Res":"100 10",
"Thichness":"200",
"number of source":"1",
"coordinate of source":[
   {"start x":"-50"},
   {"start y":"0"},
   {"end x":"50"},
   {"end y":"0"}],
"Amplitude of current":"1",
"number of electric dipoles":"10",
"number of time":"100",
"Calculated time range":"-5 -2",
"Number of receiving points":[
   {"X":"0","Y":"100","Z":"0"},
   {"X":"0","Y":"100","Z":"-10"},
   {"X":"0","Y":"100","Z":"-20"}],
"File prefix":"Model_1",
"Calculate type":"ff"}


基于Fortran编写信息提取子程序，如下：
------------------------------------