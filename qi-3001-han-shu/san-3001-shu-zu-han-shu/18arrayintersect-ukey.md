# array\_intersect\_ukey

用回调函数比较键名来计算数组的交集

```
array array_intersect_ukey ( array $array1 , array $array2 [, array $... ], callable $key_compare_func )
```

返回值：

返回一个数组，该数组包含了所有出现在`array1`中并同时出现在所有其它参数数组中的键名的值。

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

var_dump(array_intersect_ukey($array1, $array2, 'key_compare_func'));
```

```
$arr = ['a'=> 123, "b"=>456, "c"=>789];
$arr1 = ['a'=> 456];

print_r(array_intersect_ukey($arr,$arr1,"key_intersect"));

function key_intersect($a,$b) {
    if($a ==  $b) {
      return 0;
    } elseif ($a < $b) {
      return -1;
    } elseif ($a > $b) {
      return 1;
    }
}

```



