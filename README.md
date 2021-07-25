# Symfony Demo webapp

The "Symfony web Application" is a reference application created to show how
to develop applications following the [Symfony Best Practices][1].

## Requirements

- PHP 7.3 or higher;
- PDO-MYSQL PHP extension enabled;
- and the [usual Symfony application requirements][2].

## Installation

[Download Symfony][3] to install the `symfony` binary on your computer and run
this command:

```bash
$ symfony new Test_WebApp --full
```

Alternatively, you can use Composer:

```bash
$ composer create-project symfony/website-skeleton:"^3.0" Test_WebApp
```

## Usage

1. Make sure you have php 7.0 or greater
2. Install [Composer](https://getcomposer.org/download/)

3. Install [Symfony Binary](https://symfony.com/download)

4. Cd to project root and run

```bash
composer install
```

6. Set up your database connection in `.env`. postgresql, mysql, mariadb, sqlite are supported.

7. Setup database

```bash
symfony console doctrine:database:create
```

There's no need to configure anything to run the application. If you have
[installed Symfony][4] binary, run this command:

```bash
$ cd Test_WebApp/
$ symfony server:start
```

Then access the application in your browser at the given URL (<https://localhost:8000> by default).

If you don't have the Symfony binary installed, run `php -S localhost:8000 -t public/`
to use the built-in PHP web server or [configure a web server][3] like Nginx or
Apache to run the application.

I configured a XAMPP web server to run this test web app.

### Source : [XAMPP is the most popular PHP development environment.][5]

## Tests

Execute this command to run tests:

```bash
$ cd Test_WebApp/
$ ./bin/phpunit
```

[1]: https://symfony.com/doc/current/best_practices.html

[2]: https://symfony.com/doc/current/reference/requirements.html

[3]: https://symfony.com/doc/current/cookbook/configuration/web_server_configuration.html

[4]: https://symfony.com/download

[5]: https://www.apachefriends.org/index.html
