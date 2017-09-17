# array\_multisort

对多个数组或多维数组进行排序

```
bool array_multisort ( array &$array1 [, mixed $array1_sort_order = SORT_ASC [, mixed $array1_sort_flags = SORT_REGULAR [, mixed $... ]]] )
```

参数 ：

array1：需要操作的数组

array1-sort-order:

`SORT_ASC`按照上升顺序排序，

`SORT_DESC`按照下降顺序排序

array\__sort_\_flags:

排序类型标志：

* SORT\_REGULAR - 将项目按照通常方法比较（不修改类型）
* SORT\_NUMERIC - 按照数字大小比较
* SORT\_STRING - 按照字符串比较
* SORT\_LOCALE\_STRING - 根据当前的本地化设置，按照字符串比较。 它会使用 locale 信息，可以通过 setlocale\(\) 修改此信息。
* SORT\_NATURAL - 以字符串的"自然排序"，类似 natsort\(\)
* SORT\_FLAG\_CASE - 可以组合 \(按位或 OR\) SORT\_STRING 或者 SORT\_NATURAL 大小写不敏感的方式排序字符串



