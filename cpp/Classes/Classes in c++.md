c++ is a programming language that can be used both as Object-Oriented Programming (OOP), and as a Functional programming language, but most use it as the former. 

Classes are a part of OOP.

#### Extern notes

> [[Enums in c++]]
> [[Interfaces in c++]]
> [[Structs in c++]]


## Classes

Classes create a type that holds specific variables and functions.
Classes are useful for many reasons, like organizing your data and functions.
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


#### Constructors

A constructor is a method that is called when an object is initialized. It can take parameters like any other method, so it can, and is primarily, used to initialize a class' variables.

If we take our previous `Car` class and give it a constructor

###### member initializer lists


#### Destructors


### Visibility




## Other types of classes


### [[Structs in c++]]

In a few words, a struct is a class that only have a few variables, and all of it's methods only manipulate the already given data.


### [[Interfaces in c++]]

Interfaces is a class that has method requirements, so if a new class inherits from the interface, it has to include those methods

### [[Enums in c++]]

Enums is an object that
  
