## $\_FILES

通过 HTTP POST 方式上传到当前脚本的项目的数组

文件被上传后，默认地会被储存到服务端的默认临时目录中，除非 php.ini 中的 upload\_tmp\_dir

设置为其它的路径

> $\_FILES\['userfile'\]\['name'\]
>
> 客户端机器文件的原名称。
>
> $\_FILES\['userfile'\]\['type'\]
>
> 文件的 MIME 类型，如果浏览器提供此信息的话。一个例子是“_image/gif_”。不过此 MIME 类型在 PHP 端并不检查，因此不要想当然认为有这个值。
>
> $\_FILES\['userfile'\]\['size'\]
>
> 已上传文件的大小，单位为字节。
>
> $\_FILES\['userfile'\]\['tmp\_name'\]
>
> 文件被上传后在服务端储存的临时文件名。$\_FILES\['userfile'\]\['error'\]

### PHP.ini中的设置

| 名字 | 默认 | 可修改的范围 | 作用 |
| :--- | :--- | :--- | :--- |
| file\_uploads; | 1 | PHP\_INI\_SYSTEM | 是否允许HTTP上传， |
| upload\_tmp\_dir | NULL | PHP\_INI\_SYSTEM | 用户默认上传文件的临时目录，如果没有设置，使用PHP的默认值 |
| max\_input\_vars | 1000 | PHP\_INI\_PERDIR | 上传的长度限制 |
| upload\_max\_filesize | 2M |  |  |
| max\_file\_uploads | 20 |  | 允许最大上传文件数 |



