# array\_diff\_ukey

用回调函数对键名比较计算数组的差集

```
array array_diff_ukey ( array $array1 , array $array2 [, array $... ], callable $key_compare_func )
```

参数：

array：需要比较的数组

callable key ：用户自定义的回调函数

**注意：如果对于多维数组进行排序 可以深度传递**

```
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于 0 的整数。

int callback ( mixed $a, mixed $b )
```

```
<?php
function key_compare_func($key1, $key2)
{
    if ($key1 == $key2)
        return 0;
    else if ($key1 > $key2)
        return 1;
    else
        return -1;
}

$array1 = array('blue'  => 1, 'red'  => 2, 'green'  => 3, 'purple' => 4);
$array2 = array('green' => 5, 'blue' => 6, 'yellow' => 7, 'cyan'   => 8);

var_dump(array_diff_ukey($array1, $array2, 'key_compare_func'));
?>
```



