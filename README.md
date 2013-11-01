AngularJS Bundle
================

This bundle provides a base template for an AngularJS + Symfony2 project. It includes the AngularJS assets and loads them by default.

AngularJS
---------

Current version: 1.2.0-rc3

Modules included:
* angular-loader
* angular-route
* angular-cookies
* angular-sanitize
* angular-resource

Usage
-----

To use the template you just need to extend yours this way:
```jinja
{% extends 'TSAngularJSBundle::angular_base.html.twig' %}
```

To configure just add in AppKernel.php:
```php
$bundles = array(
    // ...
    new TS\AngularJSBundle\UdfAngularJSBundle(),
)
````

Edit your composer.json and add this line in the "require" object:
```json
{
    "require": {
        "rogerclotet/angularjsbundle": "1.0.*"
    }
}
```

And you should add this bundle in assetic configuration in your app/config/config.yml:
```yaml
assetic:
    bundles: [ TSAngularJSBundle ]
```

By default the AngularJS app and main controller are "myApp" and "MainCtrl". You can change their name by modifying the blocks "appname" and "maincontrollername".
