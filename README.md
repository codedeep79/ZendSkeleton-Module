# ZendSkeleton-Module
Sample skeleton module for use with the ZF3 MVC layer

## Installation

First, decide on a namespace for your new module. For purposes of this README,
we will use `MyModule`.

Clone this repository into your application:

```bash
$ cd module
$ git clone https://github.com/flightstar/ZendSkeletonModule MyModule
$ cd MyModule
```

Next, we need to setup autoloading in your application. Open the `composer.json`
file in your application root, and add an entry under the `autoload.psr-4` key:

```json
"autoload": {
    "psr-4": {
        "MyModule\\": "module/MyModule/src/"
    }
}
```

When done adding the entry:

```bash
$ composer dump-autoload
```

Finally, notify your application of the module. Open
`config/modules.config.php`, and add it to the bottom of the list:

```php
return [
    /* ... */
    'MyModule',
]
```

> ### application.config.php
>
> If you are using an older version of the skeleton application, you may not
> have a `modules.config.php` file. If that is the case, open `config/application.config.php`
> instead, and add your module under the `modules` key:
>
> ```php
> 'modules' => [
>     /* ... */
>     'MyModule',
> ],
> ```

