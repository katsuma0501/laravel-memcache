
[![Build Status](https://travis-ci.org/swiggles/laravel-memcache.svg?branch=master)](https://travis-ci.org/swiggles/laravel-memcache)

## Laravel 5 Memcache Driver

If you're on a windows PC and you're having trouble setting up memcached with laravel then this is what you need.

Handy for when you want to use a taggable cache store and test it out on your localhost.

========

### Installation

Make sure you've got both a memcached server and the memcache php extension installed.
http://stannesi.blogspot.co.uk/2011/11/how-to-install-memcache-on-xampp.html 

Add the package to your composer.json and run composer update.
```php
"swiggles/memcache": "~1.0"
```

Add the memcache service provider in app/config/app.php:

```php
'Swiggles\Memcache\MemcacheServiceProvider',
```

You may now update your config/cache.php config file to use memcache
```php
	'default' => 'memcache',
```

You may now update your config/session.php config file to use memcache

```php
	'driver' => 'memcache',
```

**Notice: This memcache driver uses the same config as Memcached**

This addon was build because of the Webtatic repo lacking Memcache Support :/
