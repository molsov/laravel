# laravel 

# laravel Installation via Composer
composer create-project --prefer-dist laravel/laravel blog "5.5.*"

# Maintenance Mode
php artisan down

php artisan down --message="Upgrading Database" --retry=60

php artisan up

# Routes 
Route::get('user/profile', 'UserController@showProfile')->name('profile');

# Middleware

Route::middleware(['first', 'second'])->group(function () {
    Route::get('/', function () {
        // Uses first & second Middleware
    });

    Route::get('user/profile', function () {
        // Uses first & second Middleware
    });
});

# Namespaces

Route::namespace('Admin')->group(function () {
    // Controllers Within The "App\Http\Controllers\Admin" Namespace
});


<form method="POST" action="/profile">
    {{ csrf_field() }}
    {{ method_field('PUT') }}
</form>

# Controllers
php artisan make:controller PhotoController --resource
