# array\_filp

交换数组中的键值

```
array array_flip ( array $array )
```

参数 ：

array 注意 array的值 必须为合法的intger 或 string 如果类型不对，**将出现一个警告 并且有问题的键／值对将不会出现在结果里。**

返回值：

交换后的数组，**失败时返回Null**

```

$arr = array("a"=>1, "b"=>2, "c"=>3, "d"=>4, "e"=>5);

print_r(array_flip($arr));

#结果：
Array ( [1] => a [2] => b [3] => c [4] => d [5] => e )
```



