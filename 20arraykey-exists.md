# array\_key\_exists

检查数组中是否存在指定的键和索引

```
bool array_key_exists ( mixed $key , array $array )
```

数组里有键 key 时，array\_key\_exists\(\) 返回 TRUE。 key 可以是任何能作为数组索引的值。

参数：

key：数组中要检查的键 ，可以为支持数组索引类型的所有值

array：需要去检查的数组

返回值：

检查key存在的时候返回true ，如果不存在或失败返回false

```
array_key_exists() 仅仅搜索第一维的键。 多维数组里嵌套的键不会被搜索到。
```

```

$arr = ['a'=> 123, "b"=>null, "c"=>789];

if (isset($arr["b"])) {
    echo "this is b in array";
}

if (array_key_exists("b", $arr)) {
    echo "this is b in array !";
}
```



