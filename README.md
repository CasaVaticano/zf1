Zend Framework 1 for Composer
=============================

This is a maintained mirror of ZF1 for use with [Packagist](http://packagist.org/packages/breerly/zf1). 

To install, add the following to your `composer.json` file:

```json
{
    "require": {
        "breerly/zf1": "*",
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

You can find the original ZF1 readme in [README.txt](README.txt)
