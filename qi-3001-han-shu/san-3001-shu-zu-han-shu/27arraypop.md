# array\_pop

弹出数组最后一个单元（出栈）

```
mixed array_pop ( array &$array )
```

参数：

array 需要操作的数组

返回值：

弹出并返回 array 数组的最后一个单元，并将数组 array 的长度减一，如果 array 是空（如果不是一个数组），将会返回 NULL 。

错误、异常：

调用此函数去处理非数组的值，会产生[E\_WARNING](http://php.net/manual/zh/errorfunc.constants.php)级别的错误

```
<?php
$stack = array("orange", "banana", "apple", "raspberry");
$fruit = array_pop($stack);
print_r($stack);
?>
```



