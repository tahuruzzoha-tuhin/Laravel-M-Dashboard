## Note

We recommend installing this preset on a project that you are starting from scratch, otherwise your project's design might break.Speed up your web development with the Bootstrap 4 Admin Dashboard built for Laravel Framework 5.5 and up.

## Prerequisites

If you don't already have an Apache local environment with PHP and MySQL, use one of the following links:

 - Windows: https://updivision.com/blog/post/beginner-s-guide-to-setting-up-your-local-development-environment-on-windows
 - Linux: https://howtoubuntu.org/how-to-install-lamp-on-ubuntu
 - Mac: https://wpshout.com/quick-guides/how-to-install-mamp-on-your-mac/

Also, you will need to install Composer: https://getcomposer.org/doc/00-intro.md   
And Laravel: https://laravel.com/docs/7.x/installation

## Installation

After initializing a fresh instance of Laravel (and making all the necessary configurations), install the preset using one of the provided methods:

### Via composer

1. `Cd` to your Laravel app  
2. Type in your terminal: `composer require laravel/ui` and `php artisan ui vue --auth`
3. Install this preset via `composer require laravel-frontend-presets/material-dashboard`. No need to register the service provider. Laravel 5.5 & up can auto detect the package.
4. Run `php artisan ui material` command to install the Argon preset. This will install all the necessary assets and also the custom auth views, it will also add the auth route in `routes/web.php`
(NOTE: If you run this command several times, be sure to clean up the duplicate Auth entries in routes/web.php)
5. In your terminal run `composer dump-autoload`
6. Run `php artisan migrate --seed` to create basic users table

### By using the archive

1. In your application's root create a **presets** folder
2. [Download an archive](https://github.com/laravel-frontend-presets/material-dashboard/archive/master.zip) of the repo and unzip it
3. Copy and paste **material-dashboard-master** folder in presets (created in step 2) and rename it to **material**
4. Open `composer.json` file 
5. Add `"LaravelFrontendPresets\\MaterialPreset\\": "presets/material/src"` to `autoload/psr-4` and to `autoload-dev/psr-4`
6. Add `LaravelFrontendPresets\MaterialPreset\MaterialPresetServiceProvider::class` to `config/app.php` file
7. Type in your terminal: `composer require laravel/ui` and `php artisan ui vue --auth`
8. In your terminal run `composer dump-autoload`
9. Run `php artisan ui material` command to install the Material preset. This will install all the necessary assets and also the custom auth views, it will also add the auth route in `routes/web.php`
(NOTE: If you run this command several times, be sure to clean up the duplicate Auth entries in routes/web.php)
10. Run `php artisan migrate --seed` to create basic users table


## Usage

Register a user or login using **admin@material.com** and **secret** and start testing the preset (make sure to run the migrations and seeders for these credentials to be available).

Besides the dashboard and the auth pages this preset also has an edit profile page. All the necessary files (controllers, requests, views) are installed out of the box and all the needed routes are added to `routes/web.php`. Keep in mind that all of the features can be viewed once you login using the credentials provided above or by registering your own user. 

### Dashboard

You can access the dashboard either by using the "**Dashboard**" link in the left sidebar or by adding **/home** in the url. 
