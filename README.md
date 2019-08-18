# PHP_Hooks
PHP_Hooks is a simple class that help to make a scalable php software, like plugins,
inspired from Wordpress

'''

function doSomething(User $user)
{
    // Do Something here with user class
}

add_action(doSomething);
'''

Somewhere in your code fire the event as follow
'''
// EventNamehere like "on.login" or Event::OnLogin
do_action("EventNameHere", $UserClass);
'''