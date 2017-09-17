# array\__count\_values_

统计数组中值出现的所有的次数

```
array array_count_values ( array $array )
```

参数：

array  需要统计的数组

返回：

返回一个关联数组，用`array`数组中的值作为键名，该值在数组中出现的次数作为值。

错误：

对于数组中每个不是string或intger类型的元素抛出异常

```
$arr = array("hello","world","!!","19","20","19"=>array(1));

$statistics = array_count_values($arr);

var_dump($statistics);

#19的地方输入了一个数组类型 会有警告

Warning: array_count_values(): Can only count STRING and INTEGER values! 
```



