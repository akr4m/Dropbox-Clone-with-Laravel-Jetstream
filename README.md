## Dropbox Clone with Laravel Jetstream

Demo Project for A Dropbox Clone with Laravel Jetstream

### Controllers

[FileController](https://github.com/akr4m/Dropbox-Clone-with-Laravel-Jetstream/blob/main/app/Http/Controllers/FileController.php)

### Web Routes

```php
<?php

use Illuminate\Support\Facades\Route;
use App\Http\Controllers\FileController;

Route::get('/', function () {
    return view('welcome');
});

Route::middleware(['auth:sanctum', 'verified'])->get('/dashboard', function () {
    return view('dashboard');
})->name('dashboard');

Route::get('/files', [FileController::class, 'index'])->name('files');
Route::get('/files/{file}', [FileController::class, 'download'])->name('files.download');

```
