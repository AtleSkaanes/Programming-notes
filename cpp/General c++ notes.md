
C++ is an older programming language from 1985, made by the Danish man Bjarne Stroustrup. Even though it is older, it is still used today in application where performance is important.

#### Extern notes

> [[Classes in c++]]

> [[Libraries]]

## Basics

### basic setup

Every c++ project needs a `main()` function of type `int`.
The code inside `main()`will run automatically, so it is from here that you will need to call other functions/classes if needed.

```cpp
int main()
{
<<<<<<< Updated upstream
=======

}
```

`int main()` returns an `int` this mean that the function must call `return` else it will fail. But in c++ this is done automatically. Meaning, if your code finished running, your main function will return a value of `0`.

This however won't work if you are using some libraries. Some libraries like #SDL for example require c syntaxing of the main function in order to run. That would look like this:
```cpp
int main(int argc, char* argv[])
{
>>>>>>> Stashed changes
	return 0;
}
```

`int main()` returns an `int` based on if the code was run successful, or if it ran into trouble.
If all went well, then it would return `0`, and every other `int` it returns means an error.

## Variables

Variables are objects that hold data.

### typesAAAAAAAAAAAAAAAA

<<<<<<< Updated upstream
Types is an important part of c++. They are used to declare what kind of variable data you are using. If it is a number like a `int` (eg. `5`) or a `float` (eg. `2.3`), or a character like a `char` (eg. `A`).
=======
Types are an important part of c++. They are used to declaring what kind of variable data you are using. If it is a number like an `int` (e.g. `5`) or a `float` (e.g. `2.3`), or a character like a `char` (e.g. `'A'`).
>>>>>>> Stashed changes

Even though they are designed to hold different data, basically the only difference between them is the amount of memory they hold.

Here is a table of the basic types, and how much data they represent.
<<<<<<< Updated upstream
| Type name | Bytes of data | Usable Bits | Max number                  | 
| --------- | ------------- | ----------- | --------------------------- |
| char      | 1             | 7           | ± 127                       |
| bool      | 1             | 8           | 255                         |
| short     | 2             | 15          | ± 32.767                    |
| int       | 4             | 31          | ± 2.147.483.647             |
| long      | 4             | 31          | ± 2.147.482.647             |
| long long | 8             | 63          | ± 9.223.372.036.854.775.807 |


## Functions


## Libraries

Libraries are a common use in c++, they are used to add extra features to the otherwise pretty barebones language. 

The most used library, that you will probably have to include in all of your projects, is `<iostream>`. It is this library that opens the ability to use the `std::` namespace, which is used for a multitude of things.

One of these things is printing to the console, which is commonly used for console apps and for debugging.

```cpp
#include <iostream>

int main()
{
	std::cout << "Hello wWrld!" << std::endl;
}
```

```output
Hello World!
```

In the example above we use the `iostream` library to print `"Hello World!"` to the console.

`Iostream` is a library made by Jerry Schwarz, that is now included in c++, so you don't have to type `.h` after it, like you have to do with your own header files (we'll get into that later), and libraries that you downloaded.
=======
| Type name   | Bytes of data | Usable Bits     | Max number                                           |
| ----------- | ------------- | --------------- | ---------------------------------------------------- |
| char        | 1             | 7               | ± 127                                                |
| bool        | 1             | 8               | 255                                                  |
| short       | 2             | 15              | ± 32.767                                             |
| int         | 4             | 31              | ± 2.147.483.647                                      |
| long        | 4 ***OR*** 8  | 31 ***OR*** 63  | ± 2.147.482.647 ***OR***  ±9.223.372.036.854.775.807 |
| long long   | 8             | 63              | ± 9.223.372.036.854.775.807                          |
| float       | 4             | 31              | 7 decimal points of accuracy                         |
| double      | 4 ***OR*** 8  | 31 ***OR*** 63  | up to 15 decimal points of accuracy                  |
| long double | 8 ***OR*** 16 | 63 ***OR*** 127 | Many points of accuracy                                                     |

The sizes of the different types are very compiler individual. But the size is easily found via this line of code: ```
```cpp
sizeof(typename);
```

## Functions
>>>>>>> Stashed changes

### Header files

