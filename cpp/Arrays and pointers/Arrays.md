## Static arrays

##### What is an array
An array is a data structure. It's used to organize multiple variables in one accessibly place. In memory the contents of the array are laid out in order and the computer finds each element by looking at your given index and the type of the array.
If the array is an integer array. Each element takes 4 bytes.
This means index 0 will be at the start position.
Index 1 will be 4 bytes out from index 0.
Index 2 will be 8 bytes.
And index 3 will be 12 bytes.

So the location of each element can be found like this:
| letter | meaning |
| ------ | ----- |
|        |       |
$$ Memory Location = i_0 + i\cdot sizeof(typename)$$


#### Create an array
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
	if (myArr.back() == "return") // the last element
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
Maps are an alternate way of storing data, they are similar to `dictionaries` from c# and `hashmaps` from java. Instead of keeping track of the elements via the stored position, like a normal array, each element has a key.
You can then search for that key in the map. And it will output the result.
```cpp
#include <iostream>
#include <string>
#include <unordered_map>

int main ()
{
  std::unordered_map<std::string,std::string> mymap;

  mymap["Bakery"] = "Barbara";  // new element inserted
  mymap["Seafood"] = "Lisa";    // new element inserted
  mymap["Produce"] = "John";    // new element inserted

  std::string name = mymap["Bakery"];   // existing element accessed (read)
  mymap["Seafood"] = name;              // existing element accessed (written)

  mymap["Bakery"] = mymap["Produce"];   // existing elements accessed (read/written)

  name = mymap["Deli"];      // non-existing element: new element "Deli" inserted!

  mymap["Produce"] = mymap["Gifts"];    // new element "Gifts" inserted, "Produce" written

  for (auto& x: mymap) {
    std::cout << x.first << ": " << x.second << std::endl;
  }

  return 0;
}
```

```output
Seafood: Barbara
Deli:
Bakery: John
Gifts:
Produce:
```

There are two types of maps, a normal map and an unordered map. The two have their own uses.

#### 'Normal' map
The map is included via `#include <map>`
The map is a map that can hold values by a key, but also in order like a regular array. So if you loop through the map via a for loop, you would get the output in order you filled the array:
Example from [Geeks for Geeks]([map vs unordered_map in C++ - GeeksforGeeks](https://www.geeksforgeeks.org/map-vs-unordered_map-c/)).
```cpp
int main()
{
	// Ordered map
	std::map<int, int> order;

	// Mapping values to keys
	order[5] = 10;
	order[3] = 5;
	order[20] = 100;
	order[1] = 1;

	// Iterating the map and
	// printing ordered values
	for (auto i = order.begin(); i != order.end(); i++)
	{
		std::cout << i->first << " : " << i->second << '\n';
	}
}

```

``` Output
1 : 1
3 : 5
5 : 10
20 : 100
```

The map sorts the input keys from lowest to highest. This way it is easy to loop over the map in order, or take elements in front or behind the current element. Generally, if the data needs to be ordered in any way, use a map.


#### Unordered Map
The unordered map is just what it sounds like. It is like the map, but the elements aren't sorted in order. This means the unordered map is faster to operate, but is less flexible. If the same example is used, this is what it would look like:
```cpp
int main()
{
	// Ordered map
	std::map<int, int> order;

	// Mapping values to keys
	order[5] = 10;
	order[3] = 5;
	order[20] = 100;
	order[1] = 1;

	// Iterating the map and
	// printing ordered values
	for (auto i = order.begin(); i != order.end(); i++)
	{
		std::cout << i->first << " : " << i->second << '\n';
	}
}

```

``` Example output
1 : 1
20 : 100
5 : 10
3 : 5
```
This is what an output could look like if the contents are looped over. They are placed randomly inside the map, where it fits best. 