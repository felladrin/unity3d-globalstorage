# GlobalStorage for Unity

Unity3D Script to store persistent data in JSON format and watch them live on Inspector.

## Features

- **Singleton implementation**. Use it from anywhere on your code, from any scene.
- **Categorization of data**. Data are categorized into Numbers, Strings, Booleans and Objects.
- **Self-instantiates on scene**. You don't need to add it to the hierarchy. As soon as it's called, it shows up on the hierarchy autmoatically. Just click on it to see the data stored.

## How to use

**Save** data to the storage:
```c#
GlobalStorage.Save("name", "John Doe");     // Saving strings.
GlobalStorage.Save("age", 28);              // Saving integers, positive and negative.
GlobalStorage.Save("experience", 473.32);   // Faving doubles/floats, positive and negative.
GlobalStorage.Save("isRunning", true);      // Saving booleans, true or false.
GlobalStorage.Save("status", playerStatus); // Saving objects. In this case, playerStatus is an instance of PlayerStatus class.
```

**Load** data from the storage:
```c#
var name = GlobalStorage.Load<string>("name");             // Note that we need to cast
var age = GlobalStorage.Load<int>("age");                  // the type of the object
var experience = GlobalStorage.Load<double>("experience"); // being recovered from the
var isRunning = GlobalStorage.Load<bool>("isRunning");     // storage. That's how the script
var status =  GlobalStorage.Load<PlayerStatus>("status");  // knows how to treat the value.
```

**Delete** data from the storage:
```c#
GlobalStorage.Delete("name");
GlobalStorage.Delete("age");
GlobalStorage.Delete("experience");
GlobalStorage.Delete("isRunning");
GlobalStorage.Delete("status");
```

## Minimum Requirements

Unity version 5.3.5f1, released 15 Mar 2016.

## License

The MIT License  
<http://victor.mit-license.org>
