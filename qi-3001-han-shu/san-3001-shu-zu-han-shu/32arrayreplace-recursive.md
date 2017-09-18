# array\_replace\_recursive

使用传递的数组递归替换第一个数组的元素

```
array array_replace_recursive ( array $array1 , array $array2 [, array $... ] )
```

array\_replace\_recursive\(\) 使用后面数组元素的值替换数组 array1 的值。 如果**一个键存在于第一个数组同时也存在于第二个数组**，**它的值将被第二个数组中的值替换**。 **如果一个键存在于第二个数组，但是不存在于第一个数组，则会在第一个数组中创建这个元素。 如果一个键仅存在于第一个数组，它将保持不变。 **如果传递了多个替换数组，它们将被按顺序依次处理，后面的数组将覆盖之前的值。

array\_replace\_recursive\(\) 是递归的：它将遍历数组并将相同的处理应用到数组的内部值。

如果数组 array1 中的值是标量，它的值将被第二个数组 array2 中的值替换，它可能是一个标量或者数组。如果 array1 和 array2 中的值都是数组，array\_replace\_recursive\(\) 函数将递归地替换它们各自的值。

参数：

array：替换的数组或数组列表

返回值：

返回一个数组。如果发生错误，将返回 NULL。

```
<?php
$base = array('citrus' => array( "orange") , 'berries' => array("blackberry", "raspberry"), );
$replacements = array('citrus' => array('pineapple'), 'berries' => array('blueberry'));

$basket = array_replace_recursive($base, $replacements);
print_r($basket);

$basket = array_replace($base, $replacements);
print_r($basket);
?>
```



