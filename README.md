# forum

`$ php artisan tinker`

```
factory('App\User')->create(['name' => 'John Doe', 'email' => 'test@example.com', 'password' => Hash::make('password')]);

$threads = factory('App\Thread', 50)->create();
$threads->each(function($thread) { factory('App\Reply', 10)->create(['thread_id' => $thread->id]); });
```
