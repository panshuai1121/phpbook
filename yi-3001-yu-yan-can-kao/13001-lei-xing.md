## PHP支持的9种原始数据类型

四种标量：

* boolean（布尔型）
* integer（整型）
* float（浮点型，也叫做double）
* string（字符串）

三种复合类型：

* array（数组）
* object （对象）
* callable（可调用）

最后两种特殊类型：

* resource （资源）
* NULL （无类型）

如果查看某个表达式的值 和类型 ，用var\_dump函数

```
<?php
$aBool = true;
$aStr = "foo";
$aStr2 = 'foo';
$aInt = 12;
//输出类型
echo gettype($aBool);
//打印类型
var_dump($aStr);
//判断是否是整型
if (is_int($aInt)) {
    $aInt += 4;
}
```



