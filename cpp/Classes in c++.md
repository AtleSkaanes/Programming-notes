
c++ is a programming language that can be used both as Object-Oriented Programming (OOP), and as a Functional programming language, but most use it as the former. 

Classes are a part of OOP.

## Classes

Classes create a type that holds specific variables and functions.
Classes are useful for many reasons, like organising your data and functions.
If you wanted to make a car with some variables in c++, you could do it like this:

```cpp
int carWheels = 4;

const char* carColor = "red";

int carMaxSpeed = 100;

int main()
{
}
```

And this is fine and all, but it would get complicated if you needed just a second car, then you would need variables like `car2wheels`, and if just looks cluttered. This is where classes come in.

```cpp
class Car
{
public:
	int wheels = 4;
	const char* color = "red";
	int maxSpeed = 100;
};  

int main()
{
	Car car1;
	Car car2;
	
    car2.color = "blue"
    
	std::cout << car1.color << car2.color << std::endl;
}
```

```output
red blue
```

In this example there are two instances of a `car`, where we only set one set of variables. But if we create two car objects, and change the color of one of them, the other one remains unchanged.

### Methods

Methods are just functions that are inside of a class. 
They are often used to manipulate the data inside the class, but they don't have to.




#### Destructors



### Structs

  

### Enums

  

### Visibility