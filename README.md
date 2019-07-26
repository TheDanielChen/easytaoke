# 介绍

淘宝联盟、京东联盟、多多进宝SDK封装。

# 使用方法
1、安装扩展包

```bash
composer require Cstopery/EasyTaoKe
```


2、执行下面的命令，然后修改config/EasyTaoKe.php

```bash
php artisan vendor:publish --provider "Cstopery\EasyTaoKe\ServiceProvider"
```

3、淘宝SDK初始化

```php
<?php
use Cstopery\EasyTaoKe\Factory;
use Cstopery\EasyTaoKe\TaoBao\Request\TbkItemInfoGetRequest;

$client = Factory::taobao ();
$req = new TbkItemInfoGetRequest;
$req->setNumIids ($numIids);
return $client->execute ($req);
```

4、京东、拼多多SDK初始化基本一样，自己摸索
