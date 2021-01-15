# Faker-Picture
[![Packagist Downloads](https://img.shields.io/packagist/dt/woodsandwalker/faker-picture?color=brightgreen)](https://packagist.org/packages/woodsandwalker/faker-picture)
[![Packagist Version](https://img.shields.io/packagist/v/woodsandwalker/faker-picture?color=brightgreen)](https://packagist.org/packages/woodsandwalker/faker-picture)

Faker-Picture is a provider for the [FakerPHP](https://github.com/FakerPHP/Faker) library to get a random image URL from [picsum.photos](https://picsum.photos).

## Getting Started

### Installation
Faker-Picture requires fakerphp/faker >= 1.12

```shell
composer require woodsandwalker/faker-picture
```
&
```shell
replace file Picture.php by mine !
```

### Basic Usage

```php
<?php

include 'vendor/autoload.php';

// use the factory to create a Faker\Generator instance
$faker = Faker\Factory::create();

// add the picture provider to Faker
$faker->addProvider(new WW\Faker\Provider\Picture($faker));

// generate a picture url
echo $faker->pictureUrl(
    640,	// width (px)
    480,	// height (px)
    false,	// grayscale (boolean)
    0,		// blur (0 = no blur, 10 = max blur)
);
// 'https://picsum.photos/640/480?random=52380'

// generate and save picture and return filepath
echo $faker->picture(
    null,	// directory to save picture (string)
    640,	// width (px)
    480,	// height (px)
    true,	// whether to return full path or just file name (boolean)
    false,	// grayscale (boolean)
    0,		// blur (0 = no blur, 10 = max blur)
);
// '/tmp/0a23be9a5ab609119e14223a22acce50.jpg'
```

## License
Faker-Picture is released under the MIT License. See the bundled LICENSE file for details.
