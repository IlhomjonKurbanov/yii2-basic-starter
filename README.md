Yii2 basic app starter template
===============================

WHAT'S SPECIAL
--------------

- Boost composer-asset-plugin update speed, more detail [here](http://www.yiiframework.com/wiki/843/boost-composer-asset-plugin-update-speed/)
- Create and use environments, more detail [here](https://www.my-yii.com/learn/view-episode/how-to-create-and-use-environments-in-yii-2-basic-application-template)
- Theming supports, guide [here](http://www.yiiframework.com/doc-2.0/guide-output-theming.html)
- Include required dependencies

  ```
  "yiisoft/yii2-imagine": "*",
  "dektrium/yii2-user": "0.9.*@dev",
  "dektrium/yii2-rbac": "1.0.0-alpha@dev",
  "froala/yii2-froala-editor": "*",
  "bower-asset/sweetalert": "*"
  ```

REQUIREMENTS
------------

The minimum requirement by this project that your Web server supports PHP 5.4.0.

Be sure your web server satisfies the requirements by run command:

```
php requirements.php
```

INSTALLATION
------------

Install [Composer](https://getcomposer.org)

```
curl -sS https://getcomposer.org/installer | php
mv composer.phar /usr/local/bin/composer
```

On Windows, you'll download and run [Composer-Setup.exe](https://getcomposer.org/Composer-Setup.exe).

Install Composer Asset Plugin

```
composer global require "fxp/composer-asset-plugin:^1.2.0"
```

Install dependencies

```
composer install
```

Create your environment configuration

```
php init
```

Can use the [built-in PHP web server](https://secure.php.net/manual/en/features.commandline.webserver.php) by running the following console command while in the project `web` directory:

```
php yii serve --port=8888
```

You can use your browser to access the installed Yii application with the following URL:

```
http://localhost:8888/
```

CONFIGURATION
-------------

### Database

Edit the file `config/web-local.php` with real data, for example:

```php
return [
    'class' => 'yii\db\Connection',
    'dsn' => 'mysql:host=localhost;dbname=yii2basic',
    'username' => 'root',
    'password' => '1234',
    'charset' => 'utf8',
];
```

**NOTES:**
- Yii won't create the database for you, this has to be done manually before you can access it.

### Running migrations

Run below command for creating database tables:

```
./yii migrate
```
