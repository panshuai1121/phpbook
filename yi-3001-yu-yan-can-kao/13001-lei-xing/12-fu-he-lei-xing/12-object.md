## 对象 object

要创建一个对象 object ，使用 new 来实例化一个类；

```
<?php 

namespace Test; //命名空间

class Test
{
    public function helloWorld() {
        echo "Hello wrold !!";
    }
}

$test = new Test();
$test->helloWorld();
```



