## How to pass the variable in blade file from controller in laravel

1. Using compact function:

The easiest way is to use the PHP `compact` function. In your controller function, define the variable and pass it to the view using `compact`. Here's an example:

```
public function index()
{
    $name = 'Najmul Hasan';
    return view('welcome', compact('name'));
}
```

In this example, we're passing `$name` variable to the `welcome.blade.php` file.

2. Using With Method:

Another way to pass a variable is to use the `with` method on the view. Here's how:

```
public function index()
{
    $name = 'Najmul Hasan';
    return view('welcome')->with('name', $name);
}
```

In this approach, we are returning the view `welcome`, and using the `with` method along with the `$name ` variable to pass it into the view.

3. Using Array:

You can also pass multiple variables using an array. Here's an example:

```
public function index()
{
    $data['name'] = 'Najmul Hasan';
    $data['age'] = 30;
    return view('welcome', $data);
}
```

In this approach, we are returning the view` welcome.` We are passing an array containing two keys, `name` and `age`. These keys contain their respective value, which will be used in the `welcome.blade.php` file using the same name.
