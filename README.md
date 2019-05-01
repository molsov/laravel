# laravel 

# laravel Installation via Composer
composer create-project --prefer-dist laravel/laravel blog "5.5.*"

# Maintenance Mode
php artisan down

php artisan down --message="Upgrading Database" --retry=60

php artisan up
