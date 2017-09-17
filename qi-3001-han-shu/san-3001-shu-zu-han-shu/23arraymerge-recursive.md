# array\_merge\_recursive

递归合并一个或多个数组

```
array array_merge_recursive ( array $array1 [, array $... ] )
```

array\_merge\_recursive\(\) 将一个或多个数组的单元合并起来，**一个数组中的值附加在前一个数组的后面。返回作为结果的数组**。

如果输入的**数组中有相同的字符串键名**，则这些值会被合并到一个数组中去，这将递归下去，因此如果一个值本身是一个数组，本函数将按照相应的条目把它合并为另一个数组。然而，如果数组具有相同的数组键名，后一个值将不会覆盖原来的值，而是附加到后面。

参数：

array：需要合并的数组

返回值：

合并后的数组

```
$arr = [
    'a'=> [
      'id' => 1,
      'name' => 'shuai',
    ],
    [
      'id' => 2,
      'name' => 'chao',
    ],
    [
      'id' => 3,
      'name' => 'jing',
    ],
    [
      'id' => 4,
      'name' => 'yuan',
    ]
];
$arr1 = [
    "a"=>[
        'id' => 1,
        'info' => [
            'address' => '南京',
        ]
     ],
     [
        'id' => 2,
        'info' => [
            'address' => '日本',
        ],
     ]
];

echo "<pre>";
print_r(array_merge_recursive($arr,$arr1));
```

结果：

```
Array
(
    [a] => Array
        (
            [id] => Array
                (
                    [0] => 1
                    [1] => 1
                )

            [name] => shuai
            [info] => Array
                (
                    [address] => 南京
                )

        )

    [0] => Array
        (
            [id] => 2
            [name] => chao
        )

    [1] => Array
        (
            [id] => 3
            [name] => jing
        )

    [2] => Array
        (
            [id] => 4
            [name] => yuan
        )

    [3] => Array
        (
            [id] => 2
            [info] => Array
                (
                    [address] => 日本
                )

        )

)
```



