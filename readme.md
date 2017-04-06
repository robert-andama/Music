<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

## How to set configure on local machine.

#### Download using Git
```bash
git clone https://github.com/trailanalytics/laravel.pmt.git
```

#### Download Zip file

- [PMT System](https://github.com/trailanalytics/laravel.pmt/archive/v5.0.zip)


#### Instructions

- Run composer install

- Run php artisan migrate --seed

- Run php artisan serve 

- Start a browser and paste [Link](http://localhost:8000/upload) where you will upload a CSV 'PMT.Fields.csv' file store in '\storage\backups'.

- Check out this file "AuthServiceProvider.php" from the "App\Providers" and 
edit this section of code.

```php

   /**
     * fetch all permissions
     * @return mixed
     */

    private function getPermissions()
    {  

        //return Permission::select('id', 'name')->with('roles')->get();  // <== uncomment this.

        return []; // <== delete this.

    }
```


## Notice

Folder    | Description
:----------|:----------
 Storage\app     | where  XML files are stored
 Storage\backups     | where all backups are stored (MysQl dumps and PMT fields file)
 Storage\exports     | where all downloaded XLS and CSV files are stored.


Credits
-------

- [Trail Analytics](https://github.com/trailanalytics)
- [All Contributors](../../contributors)

License
-------

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.