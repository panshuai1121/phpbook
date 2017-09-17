# array\_chunk

将一个数组切成多个，其中每一个数组单元数由size决定，最后一个数组单元可能少于size个

```
array array_chunk ( array $array , int $size [, bool $preserve_keys = false ] )
```

参数：

array：需要操作的数组

size：需要分成的单元数

preserve：如果为true 保存原来的键名，默认false 

