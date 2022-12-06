# TYPO3 CMS Base Distribution

Get going quickly with TYPO3 CMS.

## Prerequisites

* PHP 8.1
* [Composer](https://getcomposer.org/download/)

## Quickstart

* `composer create-project typo3/cms-base-distribution project-name ^12`
* `cd project-name`

### Setup

To start an interactive installation, you can do so by executing the following
command and then follow the wizard:

```bash
composer exec typo3 setup
```

### Setup unattended (optional)

If you're a more advanced user, you might want to leverage the unattended installation.
To do this, you need to execute the following command and substitute the arguments
with your own environment configuration.

```bash
composer exec -- typo3 setup \
    --no-interaction \
    --driver=mysqli \
    --username=typo3 \
    --password=typo3 \
    --host=127.0.0.1 \
    --port=3306 \
    --dbname=typo3 \
    --admin-username=admin \
    --admin-email="info@typo3.org" \
    --admin-user-password=password \
    --project-name="My TYPO3 Project" \
    --create-site="https://localhost/"
```

### Development server

While it's advised to use a more sophisticated web server such as
Apache 2 or Nginx, you can instantly run the project by using PHPs` built-in
[web server](https://secure.php.net/manual/en/features.commandline.webserver.php).

* `TYPO3_CONTEXT=Development php -S localhost:8000 -t public`
* open your browser at "http://localhost:8000"

Please be aware that the built-in web server is single threaded and only meant
to be used for development.

## License

GPL-2.0 or later
