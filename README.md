## After Cloning first Run
```composer install```

## Then Run
```npm install``` 
<br>
```npm run dev```

## Run Migrations
```php artisan migrate```

## Add these lines in login function
``` vendor/laravel/ui/auth-backend/AuthenticatesUser.php```<br><br>
``` $this->validateLogin($request);```<br>
```$user = User::where('email', $request->email)->first();```<br>
```if($user && $user->role_id != "2"){```<br>
``` return redirect('/login')->with('status', 'Invalid Credentials');```<br>
```}```

## Add 'user' in guard method
```return Auth::guard('user');```
