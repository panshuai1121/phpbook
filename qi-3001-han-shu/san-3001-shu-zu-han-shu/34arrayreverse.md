# array\_reverse

返回一个单元顺序相反的数组

```
array array_reverse ( array $array [, bool $preserve_keys = false ] )
```

参数：

输入的数组

preserve—key：是否保留键名，如果是数字索引始终保留

返回值：

返回反转后的数组

```

$arr = array(
  'a','b','c'
);
print_r(array_reverse($arr,true));

```

结果

```
Array ( [2] => c [1] => b [0] => a )
```



