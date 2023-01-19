
C++ is an older programming language from 1985, made by the Danish man Bjarne Stroustrup. Even though it is older, it is still used today in application where performance is important.

#### Extern notes

> [[Classes in c++]]
> [[Arrays]] 
> [[Pointers & References]]


## Basics

### basic setup

Every c++ project needs a `main()` function of type `int`.
The code inside `main()`will run automatically, so it is from here that you will need to call other functions/classes if needed.

```cpp
int main()
{

}
```

`int main()` returns an `int` this mean that the function must call `return` else it will fail. But in c++ this is done automaticly. Meaning if your code finished running, your main function will return a value of `0`.

This however won't work if you are using some libraries. Some libraries like #SDL for example require c syntaxing of the main function in order to run. That would look like this:
```cpp
int main(int argc, char* argv[])
{
	return 0;
}
```

## Variables

Variables are bits of memory that hold data.

### Types

Types are an important part of c++. They are used to declare what kind of variable data you are using. If it is a number like an `int` (eg. `5`) or a `float` (eg. `2.3`), or a character like a `char` (eg. `'A'`).

Even though they are designed to hold different data, basically the only difference between them is the amount of memory they hold. And how your computer uses them.

Here is a table of the basic types, and how much data they represent.
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
### Arrays
If you need a large quantity of variables, and you don't want to store them like this:
```cpp
int var1;
int var2;
int var3;
int var4; 
// ...
```

You can group variables in arrays. Arrays look like this:
```cpp
int myArr[] = {1, 2, 3, 4};
```
You can now access each member of the array by using `[n]` Where `n` is the index of the variable starting at 0. Go to [[Arrays]] for further details.

### Pointers and References

Go to [[Pointers & References]] for more information

## Functions


## Libraries

Libraries are a common use in c++, they are used to add extra features to the otherwise pretty barebones language. 

The most used library, that you will probably have to include in all of your projects, is `<iostream>`. It is this library that opens the ability to use some parts of the `std::` namespace, which is used for a multitude of things. In `<iostream>` you get access to both the input and output streams wich you can use to write and read from your console.

For example printing to the console, which is commonly used for console apps and for debugging looks like this:

```cpp
#include <iostream>

int main()
{
	std::cout << "Hello World!" << std::endl;
}
```

```output
Hello World!
```

In the example above we use the `iostream` library to print `"Hello World!"` to the console.

`Iostream` is a library made by Jerry Schwarz, that is now included in the c++ library, this means you don't have to type `.h` after it, like you have to do with your own header files (we'll get into that later), and libraries that you downloaded. This is implementet to tell the diffrence between c and c++ libraries since both are compapitble.

### Header files

