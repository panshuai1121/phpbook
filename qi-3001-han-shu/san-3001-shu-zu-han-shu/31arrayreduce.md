# array\_reduce

将数组回调简化成单一的值

```
mixed array_reduce ( array $array , callable $callback [, mixed $initial = NULL ] )
```

参数：

array：输入的数组

callable ：回调数组

```
mixed callback ( mixed $carry , mixed $item )
```

carry：

携带上次迭代里的值； 如果本次迭代是第一次，那么这个值是`initial`

item：

携带了本次迭代的值

inital：

如果指定了可选参数`initial`，该参数将在处理开始前使用，或者当处理结束，数组为空时的最后一个结果



