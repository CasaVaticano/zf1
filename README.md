Zend Framework 1 for Composer
=============================

This is a maintained mirror of ZF1 for use with [Packagist](http://packagist.org/packages/breerly/zf1). 

You can find the original ZF1 readme in [README.txt](README.txt)

To install, add the following to your `composer.yaml` file:

```yaml
{
    "require": {
        "breerly/zf1": "1.11.11",
    }
}
```

Then download composer and install the dependencies.

```sh
curl -s http://getcomposer.org/installer | php
php composer.phar install
```

Finally require the autoloader and you're good to go.

```php
<?php
require 'vendor/autoload.php';
Zend_Debug::dump('it worked!');
```


