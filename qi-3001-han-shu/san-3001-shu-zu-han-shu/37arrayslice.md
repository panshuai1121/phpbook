# array\_slice

从数组中取出一段

```
array array_slice ( array $array , int $offset [, int $length = NULL [, bool $preserve_keys = false ]] )
```

参数：

array:  输入的数组。

offset: 如果 offset 非负，则序列将从 array 中的此偏移量开始。如果 offset 为负，则序列将从 array 中距离末端这么远的地方开始。

length: 如果给出了 length 并且为正，则序列中将具有这么多的单元。如果给出了 length 并且为负，则序列将终止在距离数组末端这么远的地方。如果省略，则序列将从 offset 开始一直到 array 的末端。

preserve\_keys: 注意 array\_slice\(\) 默认会重新排序并重置数组的数字索引。你可以通过将 preserve\_keys 设为 TRUE 来改变此行为。



返回值：

返回其中一段。 如果 offset 参数大于 array 尺寸，就会返回空的 array





