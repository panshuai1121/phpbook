# array\_unshift

在数组开头插入一个或多个单元

```
int array_unshift ( array &$array , mixed $value1 [, mixed $... ] )
```

array\_unshift\(\) 将传入的单元插入到 array 数组的开头。注意单元是作为整体被插入的，因此传入单元将保持同样的顺序。所有的数值键名将修改为从零开始重新计数，所有的文字键名保持不变

参数：

array：输入的数组

value1：开头插入的位置

返回值：

数组新的单元数目

```
<?php
$queue = array("orange", "banana");
array_unshift($queue, "apple", "raspberry");
print_r($queue);
?>
```



