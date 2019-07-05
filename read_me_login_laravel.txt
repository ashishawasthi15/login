#quickly make a Laravel 5.2 app with Registration, Login, Password Reset and Dashboard

1- create project and Install Laravel --
composer create-project --prefer-dist laravel/laravel login

2- create login and registration ui 
php artisan make:auth

find out these file on resource->views->auth

3- create database like login

4- update db detail in .env file 

5-edit your AppServiceProvider.php file if mysql below v5.7.7 

use Illuminate\Support\Facades\Schema;

public function boot()
{
    Schema::defaultStringLength(191);
}

6- run command - for create table in database 
php artisan migrate 

after that these file created automatically in database/migration folder
Migration table created successfully.
Migrating: 2014_10_12_000000_create_users_table
Migrated:  2014_10_12_000000_create_users_table
Migrating: 2014_10_12_100000_create_password_resets_table
Migrated:  2014_10_12_100000_create_password_resets_table


7- run command in project directory - php artisan serve 

8- now registration and login working

9- in local system Reset password than please  - go .env file
mail_drive = smtp change as mail_drive = log

10- after reset your password fou find log file here take url here and paste on browser
storage -> logs   