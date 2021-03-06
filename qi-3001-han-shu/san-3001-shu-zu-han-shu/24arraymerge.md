# array\_merge

合并一个数组或多个数组

```
array array_merge ( array $array1 [, array $... ] )
```

array\_merge\(\) 将一个或多个数组的单元合并起来，一个数组中的值附加在前一个数组的后面。返回作为结果的数组。

**如果输入的数组中有相同的字符串键名，则该键名后面的值将覆盖前一个值。然而，如果数组包含数字键名，后面的值将不会覆盖原来的值，而是附加到后面。**

如果**只给了一个数组并且该数组是数字索引的，则键名会以连续方式重新索引**。

参数：

array：需要合并的数组列表

返回：

返回结果数组

```
$arr1 = array(1);
echo "<pre>";
print_r(array_merge($arr,$arr1));
```

结果

```
Array
(
    [0] => 1
)
```

如果想完全保留一个数组，只是想另外一个数组追加到前一个数组的后边可以使用+号

```
<?php
$array1 = array(0 => 'zero_a', 2 => 'two_a', 3 => 'three_a');
$array2 = array(1 => 'one_b', 3 => 'three_b', 4 => 'four_b');
$result = $array1 + $array2;
var_dump($result);
?>
```



