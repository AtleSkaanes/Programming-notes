#### Extern notes

> [[header files]]
> [[SDL]]

Libraries are a common use in c++, they are used to add extra features to the otherwise pretty bare-bones language. 

The most used library, that you will probably have to include in all of your projects, is `<iostream>`. It is this library that opens the ability to use some parts of the `std::` namespace, which is used for a multitude of things. In `<iostream>` you get access to both the input and output streams which you can use to write and read from your console.

For example, printing to the console, which is commonly used for console apps and for debugging looks like this:

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

In the example above, we use the `iostream` library to print `"Hello World!"` to the console.

`Iostream` is a library made by Jerry Schwarz, that is now included in the c++ library, this means you don't have to type `.h` after it, like you have to do with your own header files (we'll get into that later), and libraries that you downloaded. This is implemented to tell the difference between c and c++ libraries,, since both are compatible.

You can download or make your own libraries with [[header files]]

| Name    | Usecase            |
| ------- | ------------------ |
| [[SDL]] | Rendering graphics |
