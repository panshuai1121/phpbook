# array\_fill

用给定的值填充数组

```
array array_fill ( int $start_index , int $num , mixed $value )
```

参数：

start\_index: 返回数组的第一个索引

如果是负数，那么返回的数组的第一个索引将会 `start_index`，而后面索引则从0开始。

num：插入的数量

value：填充的值

返回：

填充后的数组

错误

```
如果 num 小于零，将会抛出 E_WARNING。
```

```
<?php
$a = array_fill(5, 6, 'banana');
$b = array_fill(-2, 4, 'pear');
print_r($a);
print_r($b);
?>


Array
(
    [5]  => banana
    [6]  => banana
    [7]  => banana
    [8]  => banana
    [9]  => banana
    [10] => banana
)
Array
(
    [-2] => pear
    [0] => pear
    [1] => pear
    [2] => pear
)
```



