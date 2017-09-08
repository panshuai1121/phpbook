## 生成器

生成器允许你在 [foreach](http://php.net/manual/zh/control-structures.foreach.php) 代码块中写代码来迭代一组数据而不需要在内存中创建一个数组, 那会使你的内存达到上限，或者会占据可观的处理时间。相反，你可以写一个生成器函数，就像一个普通的自定义 [函数](http://php.net/manual/zh/functions.user-defined.php)一样, 和普通函数只[返回](http://php.net/manual/zh/functions.returning-values.php)一次不同的是, 生成器可以根据需要[yield](http://php.net/manual/zh/language.generators.syntax.php#control-structures.yield)多次，以便生成需要迭代的值。



1）在普通函数中一次或者多次使用yield关键字，不返回值，只生成值，这个函数就是一个生成器。例如：

```

```

调用生成器函数的时候，PHP会返回一个属于Generator类的对象，这个对象可以使用foreach\(\)函数迭代，每次迭代，PHP会要求这个对象的实例计算并提供下一个要迭代的值，生成器的优雅之处就是在每产出一个值之后，生成器内部状态会一直停顿和恢复之间切换，直到抵达定义体的末尾或者遇到空的return;语句为止，例如：

```

```

以上例子会输出

```
value1
value2
```

2\).生成器是如何节约内存的？生成一个范围内的数值\(错误方式\)

```

```

预先创建了一个包含很大整数组成的数组，再看使用生成器的例子。

```

```

在实际的例如迭代一个4GB大小的文件中功能中，迭代器大展身手。

```

```

3\).生成器没有为PHP添加新功能，需要实现在数据集中执行快进、快退和查找，最好自己编写类实现Iterator接口，或者使用PHP标准库中的某个原生迭代器。

