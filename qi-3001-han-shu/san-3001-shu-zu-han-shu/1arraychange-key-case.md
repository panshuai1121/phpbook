# array\__change\_key\_case _

将数组中的所有键名修改为全大写或小写

语法：

```
array array_change_key_case ( array $array [, int $case = CASE_LOWER ] )
```

参数

array ：一个完整的数组

case：CASE\__UPPER CASE\_LOWER_

返回：

返回一个键全是小写或者全是大写的数组；如果输入值（`array`）不是一个数组，那么返回`FALSE`

错误/异常

如果输入值（`array`）不是一个数组，就会抛出一个错误警告（**`E_WARNING`**）。

