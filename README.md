# Missing tests for Laravel's auth module
[![Latest Stable Version](https://poser.pugx.org/dczajkowski/auth-tests/version)](https://packagist.org/packages/dczajkowski/auth-tests)
[![License](https://poser.pugx.org/dczajkowski/auth-tests/license)](https://packagist.org/packages/dczajkowski/auth-tests)

## Versioning
The version of this package reflects current major version of the Laravel framework. For example:
If Laravel framework has version 5.5, version of this package compatible will be `5.5.*`.

## Installation
```bash
composer require dczajkowski/auth-tests --dev
php artisan make:auth # if not ran previously
php artisan make:auth-tests
```

Edit `phpunit.xml` file by adding these two lines between `<php>` tags:
```xml
<env name="DB_CONNECTION" value="sqlite"/>
<env name="DB_DATABASE" value=":memory:"/>
```
Alternatively, use different database than sqlite, but also different from the one used for development.

## Updating
To update tests when a new version of this package arrives:
```bash
composer update dczajkowski/auth-tests
php artisan make:auth-tests --force
```
**Warning! All changes to the files this package provides will be lost when running this command!**

## Automate your workflow
Instead of including this package manually every project you create, simply create a bash function that will do that for you. I have included my personal function [here](https://gist.github.com/DCzajkowski/9ebaeaa09d136e77497e060449b03171). Feel free to edit it and reuse however you like.

## Contributing
Feel free to make PRs to this repo.

## License
License can be found in the `LICENSE` file. It is a simple MIT, which basically means -- use it however you like.
