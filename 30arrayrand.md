# array\_rand

从数组中随机取出一个或多个单元，并返回随机条目的一个或多个键。 **它使用了伪随机数产生算法，所以不适合密码学场景**

```
mixed array_rand ( array $array [, int $num = 1 ] )
```

参数：

array：输入数组

int：取出的随机单元

返回值：

如果只取出一个，array\_rand\(\) 返回随机单元的键名。 否则就返回包含随机键名的数组。 完成后，就可以根据随机的键获取数组的随机值。 取出数量如果超过 array 的长度，就会导致 E\_WARNING 错误，并返回 NULL。

```
$arr = (range(1,100));
$randKeys = array_rand($arr,10);
print_r($randKeys);
```



