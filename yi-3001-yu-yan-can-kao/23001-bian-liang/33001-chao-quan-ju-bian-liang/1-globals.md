## $GLOBALS

一个包含了全部变量的全局组合 ，数组超全局变量、使用时变量的名称就是数组的键

```
<?php
function test() {
    $foo = "local variable";

    echo '$foo in global scope: ' . $GLOBALS["foo"] . "\n";
    echo '$foo in current scope: ' . $foo . "\n";
}

$foo = "Example content";
test();
```



