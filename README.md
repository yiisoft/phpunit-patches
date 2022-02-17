# Legacy PHPUnit patches

Patches for PHPUnit 4.8.34 allowing it to run on PHP 5.3 - PHP 8.1.

You can apply these automatically with [Simple patches plugin for Composer](https://github.com/cweagans/composer-patches) in your `composer.json`:

```json
{
    "require-dev": {
        "cweagans/composer-patches": "^1.7",
        "phpunit/phpunit": "4.8.34"
    },
    "extra": {
        "composer-exit-on-patch-failure": true,
        "patches": {
            "phpunit/phpunit-mock-objects": {
                "Fix PHP 7 and 8 compatibility": "https://github.com/longthanhtran/phpunit-patches/blob/main/phpunit_mock_objects.patch"
            },
            "phpunit/php-file-iterator": {
                "Fix php-path-file deprecate warn": "https://github.com/longthanhtran/phpunit-patches/blob/main/phpunit_path_file_iterator.patch"
            },
            "phpunit/php-file-iterator": {
                "Fix PHP 8.1 compatibility": "https://yiisoft.github.io/phpunit-patches/phpunit_path_file_iterator.patch"
            },
            "phpunit/phpunit": {
                "Fix PHP 7 compatibility": "https://yiisoft.github.io/phpunit-patches/phpunit_php7.patch",
                "Fix PHP 8 compatibility": "https://yiisoft.github.io/phpunit-patches/phpunit_php8.patch",
                "Fix PHP 8.1 compatibility": "https://yiisoft.github.io/phpunit-patches/phpunit_php81.patch"
            }
        }
    }
}
```
