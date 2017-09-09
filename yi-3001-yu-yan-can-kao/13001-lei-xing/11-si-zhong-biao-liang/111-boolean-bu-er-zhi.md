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



