# array\_keys

返回数组中部分键名，或全部键名

```
array array_keys ( array $array [, mixed $search_value = null [, bool $strict = false ]] )
```

参数：

array：需要返回键名的数组

search-value：如果设置该参数，只会返回存在该值的键名

strict：是否进行严格检查 ===

返回值：

返回`input`里的所有键

```
$arr = ['a'=> 123, "b"=>'b', "c"=>789,"B"=>'B'];

print_r(array_keys($arr,'b',true));
```

结果

```
Array ( [0] => b )
```



