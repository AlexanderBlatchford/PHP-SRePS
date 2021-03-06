

# PHP-SRePS
Sales Reporting and Prediction System	(PHP-­SRePS)

## Requirements
* Composer
* PHP7.2 (and sub-modules)
* Laravel (optional: for local testing)

## Setup
Clone the project  
```bash
git clone https://github.com/ljackl/PHP-SRePS.git
```

Install project dependencies (from within project directory)  
```bash
composer install
```

Create a local .env copy  
```bash
cp .env.example .env
```

Generate encryption key  
```bash
php artisan key:generate
```

Edit database connection properties  
```
DB_DATABASE=php_sreps_db
DB_USERNAME=root
DB_PASSWORD=
```

Create the database either using phpMyAdmin or from the command line  
```sql
CREATE databse php_sreps_db
```

Create the tables using Laravel Migrations  
```bash
php artisan migrate
```
or to refresh  
```bash
php artisan migrate:fresh
```

Seed the database  
```bash
composer dump-autoload
php artisan db:seed
```

## Running
Ensure Apache and MySQL are running in XAMPP

### Option 1:
Run from within the PHP-SRePS project
```bash
php artisan serve
```
Browse to `localhost:8000`

### Option 2:
Copy the Laravel project into XAMPP's htdocs folder and browse to it  
`localhost/PHP-SRePS/public/`
