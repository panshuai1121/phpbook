# array\_intersect

计算数组的交集

```
array array_intersect ( array $array1 , array $array2 [, array $... ] )
```

参数：

array:需要计算交集的数组

返回值：

该数组包含了所有在`array1`中也同时出现在所有其它参数数组中的值。

```
<?php
$array1 = array("a" => "green", "red", "blue");
$array2 = array("b" => "green", "yellow", "red");
$result = array_intersect($array1, $array2);
print_r($result);
```



