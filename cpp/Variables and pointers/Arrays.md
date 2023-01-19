## Static arrays

#### Create an array
An array is a data structure. It's used to organize multiple variables in one accessibly place. A regular array can be made like this:
```cpp
int arrName[Optional size] = {1, 2, 3, 15};
```
If you don't give the array a size, the array will get a size matching the number of variables it was holding when it was declared. If you try to access an index that is out of range you will get errors.

#### Access an array
To access an array in c++ you use the square brackets: '`[]`' and type your index (starting at 0) in the brackets:
```cpp
int index = 2;
float myArr[5] = {2.5f, 1.0f, 4,6f, 8.12f};

std::cout << myArr[3] << std::endl;
std::cout << myArr[index] << std::endl;
```

```output
8.12
4.6
```

If you wish to change a part of the array simply use `[]` again and this time set or change the value:
```cpp
myArr[1] *= 5;
myArr[4] = 420.69f;
```

```myArr
	2.5f, 5.0f, 4,6f, 8.12f, 420.69f
```

#### Finding the length of your array
This isn't very useful with static arrays like in the previous examples, but it can be done.
To find the length of your array you must find the size of it, and then divide that by the size of it's datatype:
```cpp
std::cout << "The size of myArr is " << sizeof(myArr) / sizeof(float) << std::endl;
```

```output
The size of myArr is 5
```

Although this approach does work it is very vulnerable and should be avoided. Instead you should manually type in the length of your array.

### Smarter arrays
There is a way to create smarter static arrays. This however comes with some overhead, meaning it takes more memory. You can include the header file `array` and get access to `std::array`.
Look under [[header files]] for more details of headers. 

The smart array comes with a wide range of functions. For example can you now find the size with a simple `.size()` function. You can also get iterators to the beginning and end of the array.

## Dynamic arrays
A dynamic array is an array that can grow and shrink in size. This is useful when the data to be stored has a variable size, that can't be determined during compile time. To use a dynamic array in c++ include the header: `vector`.
A std vector is made like so:
```cpp
#include <vector>

std::vector<typename> myDynamicArr;
```

A vector can be used just like a regular static array via square brackets `[]`. 
Here is an example using a std vector:
```cpp
std::vector<const char*> myArr;

while(true)
{
	myArr.push_back(std::cin);
	if (myArr.back() == "return")
		break;
}
std::cout << myArr[3] << std::endl;
```

```input
> Test
> Hello
> World
> Dynamic
> Array
> return
```

```output
Dynamic
```
In the example above the myArr array will take inputs of words from the console until the user types `"return"` then the program will end.
Go to [CPlusPlus](https://cplusplus.com/reference/vector/vector/) for a detailed guide of all the functions that come included in the vector header.

## Maps
