# array\_\_diff\_\_assoc

带索引计算数组中的差值

```
array array_diff_assoc ( array $array1 , array $array2 [, array $... ] )
```

参数：

array ：需要比较的数组

返回：

返回一个数组，其中不包含在数组1中存在的值

```
$arr1 = array("hello","world","!!","19","20","19");
$arr2 = array("hello","array","boolean","double");
$arr3 = ["world","100","array"];

$result = array_diff_assoc($arr1, $arr2, $arr3);

print_r($result);
```

注意：

1、**比较时值之间的索引位置也必须相同**

