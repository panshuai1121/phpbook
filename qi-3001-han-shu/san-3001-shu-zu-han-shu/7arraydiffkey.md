# array\_\_diff\_\_key

使用键名比较计算数组的差集

```
array array_diff_key ( array $array1 , array $array2 [, array $... ] )
```

参数：

比较的数组

返回值：

**array\_diff\_key\(\) **返回一个数组，该数组包括了所有出现在`array1`中但是未出现在任何其它参数数组中的键名的值

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

$result = array_diff_key($arr1, $arr2);

print_r($result);
```



