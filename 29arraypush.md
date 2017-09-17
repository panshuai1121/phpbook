# array\_push

将一个或多个单选压入数组的末尾（入栈）

```
int array_push ( array &$array , mixed $value1 [, mixed $... ] )
```

array\_push\(\) 将 array 当成一个栈，并将传入的变量压入 array 的末尾。array 的长度将根据入栈变量的数目增加。和如下效果相同：

```
<?php
$array[] = $var;
?>
```

并对每个传入的值重复以上动作。

**如果第一个参数不是数组，array\_push\(\)将发出一条警告。这和$var\[\]的行为不同，后者会新建一个数组**

参数：

array：输入的数组

value：压入数组末尾的值

返回值：

返回处理之后数组的元素个数



