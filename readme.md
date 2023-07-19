## 安装
`composer require guanhui07/geohash`

## 用法
```php
use Guanhui07/GeoHash;

$geohash = new Geohash();
//得到这点的hash值
$hash = $geohash->encode(39.98123848, 116.30683690);
//取前缀，前缀约长范围越小
$prefix = substr($hash, 0, 6);
//取出相邻八个区域
$neighbors = $geohash->neighbors($prefix);
array_push($neighbors, $prefix);

print_r($neighbors);
```
得到9个geohash值
//得到9个geohash值

Array
(
[top] => wx4eqx
[bottom] => wx4eqt
[right] => wx4eqy
[left] => wx4eqq
[topleft] => wx4eqr
[topright] => wx4eqz
[bottomright] => wx4eqv
[bottomleft] => wx4eqm
[0] => wx4eqw
)



其他资料：

geohash演示: http://openlocation.org/geohash/geohash-js/
wiki: http://en.wikipedia.org/wiki/Geohash
原理: https://github.com/CloudSide/geohash/wiki



## 我的其他包：
https://github.com/guanhui07/dcr  借鉴Laravel实现的 PHP Framework ，FPM模式、websocket使用的workerman、支持容器、PHP8特性attributes实现了路由注解、中间件注解、Laravel Orm等特性

https://github.com/guanhui07/redis Swoole模式下 Redis连接池

https://github.com/guanhui07/facade  facade、门面 fpm模式下可使用

https://github.com/guanhui07/dcr-swoole-crontab 基于swoole实现的crontab秒级定时任务

https://github.com/guanhui07/database  基于 illuminate/database 做的连接池用于适配Swoole的协程环境

https://github.com/guanhui07/dcr-swoole  高性能PHP Framework ，Cli模式，基于Swoole实现，常驻内存，协程框架，支持容器、切面、PHP8特性attributes实现了路由注解、中间件注解、支持Laravel Orm等特性