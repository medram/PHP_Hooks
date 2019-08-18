# PHP_Hooks
PHP_Hooks is a simple class that help to make a scalable php software, like plugins,
inspired from Wordpress & I hope that help someone :D

## Useful Functions:
```
- add_action($name, $function, $priority = 10)
- do_action($name, $arguments = NULL)
- remove_action($name, $function, $priority = 10)
- add_filter($name, $function, $priority = 10)
- do_filter($name, $arguments)
- remove_filter($name, $function, $priority = 10)
```

### note:
The filters function have to return something.

### action example
```
function doSomething(User $user)
{
    // Do Something here with user class
}

add_action(doSomething);
```

Somewhere in your code fire the event as follow
```
// EventNamehere like "on.login" or Event::OnLogin
do_action("EventNameHere", $UserClass);
```
### filter example
```
add_filter('BlogTitleName', function ($title){
    return "<h1>{$title}</h1>";
});
```

```
$blogTitle = "Assassin's Creed in 2019 !"

$newBlogTitle = do_filter('BlogTitleName', $blogTitle);
echo $newBlogTitle
// result: <h1>Assassin's Creed in 2019 !</h1>
```

