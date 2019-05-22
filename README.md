# Laravel 5.8 - Boilerplate
Laravel tips and ribs

## Formas de crear un proyecto

* Composer

        composer create-project --prefer-dist laravel/laravel <project-name>

* Laravel CLI

        laravel new <project-name>

## Permisos requeridos

* Hay carpetas que requieren permisos de escritura por parte del sistema

        sudo chown -R salvadoralfocea storage bootstrap/cache
    
## Modelos y controladores

* Crear un nuevo controlador

        php artisan make:controller <UserController>
        
    Fuente: https://laravel.com/docs/5.8/controllers
        
* Crear un nuevo modelo

        php artisan make:model <User>
        
* Crear un nuevo modelo y un controlador asociado

        php artisan make:model <User> -mc
    Esto da como resultado las clases *User.php* y *UserController.php*
    
    Fuente: https://laravel.com/docs/5.8/eloquent
    
    
## Migraciones
    
* Crear una migración

        php artisan make:migration create_users_table
        
* Lanzar las migraciones

        php artisan migrate
        
    Fuente: https://laravel.com/docs/5.8/migrations

## Extra

* Entre los diferentes "scaffold" que nos ofrece Laravel, se encuentra el de autenticación y manejo de usuarios. 
Para implementarlo es tan sencillo como ejecutar:

        php artisan make:auth
    Tras este comando es necesario lanzar las migraciones de base de datos.
    
    Fuente: https://laravel.com/docs/5.8/authentication