# array\_map

为数组每个元素应用回调函数

```
array array_map ( callable $callback , array $array1 [, array $... ] )
```

参数：

callable：处理数组每一个元素的回调函数

array：需要处理的数组

返回值：

回数组，包含 callback 函数处理之后 array1 的所有元素。

**注意：**

**需要处理多个数组时，callback函数的参数，必须与处理数组列表的数量相同**

返回值：

返回数组，**包含callback 处理之后的array1数组的所有元素**

```
$arr = ['a'=> "a", "b"=>'b', "c"=>"c","B"=>'B',"D"=>'d','E'=>'e',"F"=>'f'];
$arr1 = [0,1,2,3,4,5];

$arr2 = array_map(function($a,$b) {
  $a = strtoupper($a);
  return "this is number '{$b}' the content '{$a}' ";
}, $arr,$arr1);

print_r($arr2);
```



