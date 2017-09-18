# array\_splice

去掉数组中的某一部分并用其它值取代

```
array array_splice ( array &$input , int $offset [, int $length = count($input) [, mixed $replacement = array() ]] )
```

把 input 数组中由 offset 和 length 指定的单元去掉，如果提供了 replacement 参数，则用其中的单元取代。

**注意 input 中的数字键名不被保留**。

参数：

input

输入的数组。

offset

如果 offset 为正，则从 input 数组中该值指定的偏移量开始移除。如果 offset 为负，则从 input 末尾倒数该值指定的偏移量开始移除。

length

如果省略 length，则移除数组中从 offset 到结尾的所有部分。如果指定了 length 并且为正值，则移除这么多单元。如果指定了 length 并且为负值，则移除从 offset 到数组末尾倒数 length 为止中间所有的单元。 如果设置了 length 为零，不会移除单元。 小窍门：当给出了 replacement 时要移除从 offset 到数组末尾所有单元时，用 count\($input\) 作为 length。

replacement

如果给出了 replacement 数组，则被移除的单元被此数组中的单元替代。

如果 offset 和 length 的组合结果是不会移除任何值，则 replacement 数组中的单元将被插入到 offset 指定的位置。 注意替换数组中的键名不保留。

如果用来替换 replacement 只有一个单元，那么不需要给它加上 array\(\)，除非该单元本身就是一个数组、一个对象或者 NULL。



