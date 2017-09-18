# array\_replace

使用传递的数组替换第一个数组的元素

```
array array_replace ( array $array1 , array $array2 [, array $... ] )
```

array\_replace\(\) 函数**使用后面数组元素相同 key 的值替换 array1 数组的值**。如果**一个键存在于第一个数组同时也存在于第二个数组，它的值将被第二个数组中的值替换**。如果**一个键存在于第二个数组，但是不存在于第一个数组，则会在第一个数组中创建这个元素**。如果**一个键仅存在于第一个数组，它将保持不变**。如果传递了多个替换数组，它们将被按顺序依次处理，后面的数组将覆盖之前的值。

**array\_replace\(\) 是非递归的：它将第一个数组的值进行替换而不管第二个数组中是什么类型。**

参数：

array1：需要替换的数组

array2：从数组中取替换的值

返回值：

返回一个数组。如果发生错误，将返回`NULL`。

```
<?php
$base = array("orange", "banana", "apple", "raspberry");
$replacements = array(0 => "pineapple", 4 => "cherry");
$replacements2 = array(0 => "grape");

$basket = array_replace($base, $replacements, $replacements2);
print_r($basket);
?>
```



