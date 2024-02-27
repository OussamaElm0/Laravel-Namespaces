# Laravel-Namespaces
Laravel basics namespaces

## Routes, Controllers, Middleware, Requests, Eloquent ORM, and Query Builders

Routes in Laravel are defined using the `Illuminate\Routing\Router` class. This class provides methods like `get()`, `post()`, `put()`, `delete()`, etc., for defining HTTP verbs. These methods return instances of `Illuminate\Routing\Route` class.

### Routes:
```php
use Illuminate\Support\Facades\Route;

Route::get('/hello', function () {
    return 'Hello, World!';
});
```

### Controllers:
```php
namespace App\Http\Controllers;

use Illuminate\Routing\Controller;

class UserController extends Controller
{
    //
}
```
### Middlewares: 
```php
namespace App\Http\Middleware;

use Closure;

class ExampleMiddleware
{
    public function handle($request, Closure $next)
    {
        // Perform action before the request is passed further
        return $next($request);
    }
}
```
### Requests: 
```php
use Illuminate\Http\Request;
```

### Models:
```php
namespace App\Models;

use Illuminate\Database\Eloquent\Model;

class User extends Model
{
    //
}
```
### Query Builder:
```php
use Illuminate\Support\Facades\DB;

$users = DB::table('users')->where('active', true)->get();

```
