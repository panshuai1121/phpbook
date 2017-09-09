## boolean 布尔

计算机科学中的逻辑数据类型，以发明布尔代数的数学家 乔治·布爾 为名,它是两种值的原始类型 ，通常是True和False。

指定布尔值，通常使用TRUE或FALSE。两个都区分大小写

```
<?php

if ($action == "show_version") {
    echo "The version is 1.23";
}

if ($show_version) {

}
```

### 转换布尔值

当转换为 boolean的时候 可以使用（bool） \(boolean\) 来强制转换。但很多情况不用强制转换，控制流程结构需要一个boolea参数时 boolean，该值会自动转换。

当转换bool值，以下为false；

```
// 1 布尔值 false 本身
var_dump((bool) false);
// 2 整型值 0
var_dump((bool) 0);
// 3 浮点型值  0.0
var_dump((bool) 0.0);
// 4 空字符串，以及字符串 0
var_dump((bool) "");
var_dump((bool) '0');
// 5 不包括任何元素的数组
var_dump((bool) []);
// 6 特殊类型  NULL
var_dump((bool) NULL);
// 7 空标记生成的simpleXML 对象
```



