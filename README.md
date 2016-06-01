Yii2 outdated-browser
=====================

Usage of this plugin is really simple, just include it in your `composer.json` like so:

```
php composer.phar require --prefer-dist pashkinz92/yii2-outdated-browser "*"
```



``` php
<?= pashkinz92\outdatedBrowser\OutdatedBrowser::widget() ?>
```

## Setting the parameters

The outdated browser plugin accepts four parameters which can be provied as class vars like so:

```php
<?= pashkinz92\outdatedBrowser\OutdatedBrowser::widget(['language' => 'ar', 'bgColor' => '#f25648']) ?>
```

## Using this only for IE7

Using this only for IE7 can be very useful especially since Bootstrap 3.x supports IE8+

Since Yii2, by default, only uses JQuery 2.2 you must actually add a line to your composer to make this work:

``` bash
"bower-asset/jquery": "~1.11@stable",
```

And then when calling the plugin you simply put:

``` php
<?= pashkinz92\outdatedBrowser\OutdatedBrowser::widget(['onlyIe7' => true]) ?>
```