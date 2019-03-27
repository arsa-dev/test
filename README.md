# Vtiger Prototype

This project connects via API and send data to vtiger instance. Working on vtiger v7.x

## Getting Started

To run this project you have to download it and push it into a web server with PHP.

### Prerequisites

To run this software is needed an apache web server with PHP support, and a available connection to vtiger instance, setted in init.php

### Installing

To install a new instance of vtiger-prototype you need to follow the next steps:

Copy all files to accesible web server, for example:

```
http://localhost/vtiger-prototype/
```

Then replace the following config lines at init.php as in the example

```
// Set global config object
$config = (object)[
    "username" => "<VTIGER_USERNAME>", // Used for api login
    "apikey" => "<VTIGER_USER_API_KEY>"  // Used for api login
];
// Configure webservice endpoint
define('URL', "<YOUR_VTIGER_API_ENDPOINT>");
```

## Deployment

To deploy vtiger-prototype do the same steps exposed in Installing with production config.

### Project structure

```
 - vendor/ -> Used by composer 
 - views/ -> Place to store app views and view controller
 - init.php -> Config and app initialization file
 - func.php -> Used for common and util functions
 - *.php -> Public files for app functionality
```

## Built With

* [PHP](http://php.net/) - The programming language used
* [Composer](https://getcomposer.com/) - Dependency Management

### Dependencies h3

* [php-restclient](https://github.com/tcdent/php-restclient) - Used to make api calls easily without using CURL or something else.

## Authors

* **Antonio Ramón** - *Initial work* - [ramon@bmsoft.de](ramon@bmsoft.de)

## Acknowledgments

* The forms data will be send to the vtiger instance setted in init.php, by default it is a public demo instance of [vtexperts.com](vtexperts.com). It is used only for testing purposed
