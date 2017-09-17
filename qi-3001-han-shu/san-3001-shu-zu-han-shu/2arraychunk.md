# array\_chunk

将一个数组切成多个，其中每一个数组单元数由size决定，最后一个数组单元可能少于size个

```
array array_chunk ( array $array , int $size [, bool $preserve_keys = false ] )
```

参数：

array：需要操作的数组

size：需要分成的单元数

preserve：如果为true 保存原来的键名，默认false，从0开始重新计算索引

```
$arr  = [
    'a' => array(1),
    'b' => array(2),
    'c' => array(3),
    array(4),
    array(
      5 => array(6)
    ),
];

$newArr = array_chunk($arr, 2,true);

#结果
Array
(
    [0] => Array
        (
            [a] => Array
                (
                    [0] => 1
                )

            [b] => Array
                (
                    [0] => 2
                )

        )

    [1] => Array
        (
            [c] => Array
                (
                    [0] => 3
                )

            [0] => Array
                (
                    [0] => 4
                )

        )

    [2] => Array
        (
            [1] => Array
                (
                    [5] => Array
                        (
                            [0] => 6
                        )

                )

        )

)
```



