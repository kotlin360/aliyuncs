Aliyuncs for php 
--------------------------------
就是一个封装了阿里云图片鉴黄，涉政暴恐，场景API的composer包，给自己用的。。。。。

## Contents
- [Installation](#installation)
- [Example](#example)

## Installation

With composer

```bash
composer require llwch/aliyuncs
```

Or add

```json
"llwch/aliyuncs": "dev-master"
```

to your composer.json. Then run `composer install` or `composer update`.

## Example

An example of how to used:

```php
<?php

use AliyunCs\Client\ImageSyncScanRequestClient;

class ImageSyncScan
{
    public function handle()
    {
        $accessKey = 'xxxxxxxxxxxxx';
        $secretKey = 'xxxxxxxxxxxxx';
        $handleImg = 'http://www.xxxx.com/xxx.jpg';
        $handleImg = [
            'http://www.xxxx.com/xxx.jpg',
            'http://www.xxxx.com/xxx.jpg'
        ];
        $imageSyncScanResults = (new ImageSyncScanRequestClient($accessKey, $secretKey))->request($handleImg);
        
        //TODO;
    }
}
```