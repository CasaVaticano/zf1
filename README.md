Zend Framework 1 for Composer
=============================

This is a maintained mirror of ZF1 for use with [Packagist](http://packagist.org/packages/breerly/zf1). You can find the original ZF1 readme in README.txt

Why maintain a mirror? Because we love Github & Composer - it's just a better experience than the official [Subversion Repository](http://framework.zend.com/code/listing.php?repname=Zend+Framework).

## Installation

To install, add the following to `composer.json` at the root of your project:

```json
{
    "require": {
        "breerly/zf1": "1.11.*",
    }
}
```

Then download composer and install the dependencies.

```sh
curl -s http://getcomposer.org/installer | php
php composer.phar install
```

### Using ZF Components standalone

Require the autoloader and you're good to go.

```php
<?php
require 'vendor/autoload.php';
Zend_Debug::dump('it worked!');
```

### Setting up an entire Zend Framework Project

Use ZF's cli to setup your project.

```sh
php vendor/bin/zf.php --help
php vendor/bin/zf.php create project . myproject
```

Now install vendors.

```sh
curl -s http://getcomposer.org/installer | php
php composer.phar install
```

You'll want to add the vendors folder to your `.gitignore`

```sh
echo vendors >> .gitignore
```

Then at the top of `public/index.php` require the autoloader.

```php
<?php
require_once __DIR__ . '/../vendor/autoload.php';
// ...
```

And finally, if you do not plan on using ZF's library convention and instead plan on using Composer across the board, you should disable `Zend_Loader_Autoloader` by adding this line in `public/index.php` before the application is bootstrapped.

```php
<?php
// ...
spl_autoload_unregister(array('Zend_Loader_Autoloader','autoload'));
$application->bootstrap()->run();
```
