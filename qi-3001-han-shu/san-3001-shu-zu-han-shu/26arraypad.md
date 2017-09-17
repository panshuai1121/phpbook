# array\_pad

以指定长度将一个值填充进数组

```
array array_pad ( array $array , int $size , mixed $value )
```

array\_pad\(\) 返回 array 的一个拷贝，并用 value 将其填补到 size 指定的长度。如果 size 为正，则填补到数组的右侧，如果为负则从左侧开始填补。如果 size 的绝对值小于或等于 array 数组的长度则没有任何填补。有可能一次**最多填补 1048576 个单元**。

参数：

array ：需要填充的数组

size：新数组的长度

value：填充的值，只有在array的长度小于size时生效

返回值：

返回 array 用 value 填充到 size 指定的长度之后的一个副本。 如果 size 为正，则填补到数组的右侧，如果为负则从左侧开始填补。 如果 size 的绝对值小于或等于 array 数组的长度则没有任何填补。

```
<?php
$input = array(12, 10, 9);

$result = array_pad($input, 5, 0);
// result is array(12, 10, 9, 0, 0)

$result = array_pad($input, -7, -1);
// result is array(-1, -1, -1, -1, 12, 10, 9)

$result = array_pad($input, 2, "noop");
// not padded
?>
```



