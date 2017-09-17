# array\_diff

计算数组中值的差集

```
array array_diff ( array $array1 , array $array2 [, array $... ] )
```

参数：

需要比对的数组

返回值：

返回一个数组，该数组包括了所有在`array1`中，但是不在任何其它参数数组中的值。注意**键名保留不变**。

```
$arr1 = array(
    'name' => 'job',
    'id' => 123,
    'class'=>9,
);
$arr2 = array(
    'name' => 'jk',
    'id'  => 141,
    'age' => 15
);

print_r(array_diff($arr1,$arr2));

#结果
Array ( [name] => job [id] => 123 [class] => 9 )
```



