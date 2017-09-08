## trait

性状的诞生是为了解决，让无关的类具有共同的行为。

> 性状是类的部分实现\(常量、属性和方法\)，可以混入一个或者多个现有的PHP类中，性状有两个作用，表明类可以做什么\(类似接口\)，提供模块化实践\(类似类\)。
>
> 性状使得两个无关的类可以使用相同属性和方法。
>
> .PHP解释器会把性状复制粘贴到类的定义体中。

设计需要符合：**DRY（Dont‘t Repeat Yourself），表示不要在多个地方重复编写相同的代码。**



```
<?php
trait World {

    private static $instance;
    protected $tmp;

    public static function World()
    {
        self::$instance = new static();
        self::$instance->tmp = get_called_class().' '.__TRAIT__;

        return self::$instance;
    }

}

if ( trait_exists( 'World' ) ) {

    class Hello {
        use World;

        public function text( $str )
        {
            return $this->tmp.$str;
        }
    }

}

echo Hello::World()->text('!!!'); // Hello World!!!
```



