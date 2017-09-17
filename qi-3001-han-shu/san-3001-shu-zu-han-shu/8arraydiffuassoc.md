# array\__diff\_uassoc_

用用户提供的回调函数做索引检查来计算数组的差集

```
array array_diff_uassoc ( array $array1 , array $array2 [, array $... ], callable $key_compare_func )
```

参数：

array 对别的数组

callable ：用户定义的回调函数

int callback\([mixed](http://php.net/manual/zh/language.pseudo-types.php#language.types.mixed)`$a`,[mixed](http://php.net/manual/zh/language.pseudo-types.php#language.types.mixed)`$b`\)

返回值：

返回一个 array，该数组包括了所有在 array1 中但是不在任何其它参数数组中的值。

```
<?php
function key_compare_func($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b)? 1:-1;
}

$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "yellow", "red");
$result = array_diff_uassoc($array1, $array2, "key_compare_func");
print_r($result);
?>
```



