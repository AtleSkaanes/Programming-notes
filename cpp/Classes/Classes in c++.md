c++ is a programming language that can be used both as Object-Oriented Programming (OOP), and as Functional programming, but most use it as the former. 

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
	std::string color = "red";
	int maxSpeed = 100;
};  

int main()
{
	Car car1;
	Car car2;
	
    car2.color = "blue"
    
	std::cout << car1.color << " " << car2.color << std::endl;
}
```

```output
red blue
```

In this example, there are two instances of a `car`, where we only set one set of variables. But if we create two car objects, and change the color of one of them, the other one remains unchanged.

### Members
A member is another word for a variable that is contained inside a class. These variables, no matter, their visibility can be accessed by all the classes functions also named methods.


### Methods

Methods are just functions that are inside a class. 
They are often used to manipulate the data inside the class, but they don't have to.
A method works just like any other function, where you can give them parameters and a return type. But methods have one more thing. They have an invisible pointer to the class it is contained in, which means you have access to all the class variables, even private ones.


#### Constructors

A constructor is a method that is called when an object is initialized. It can take parameters like any other method, so it can, and is primarily, used to initialize a class's variables.

You can make a constructor by making a method with no type (not even void), and then give it the exact same name as the class, like this:
```cpp
class Object
{
	Object()
	{
		// This is the constructor
	}
};
```


If we take our previous `Car` class and give it a constructor, the class could look something like this:

```cpp
class Car
{
public:
	int wheels;
	std::string color;
	int maxSpeed;
	
	Car(int wheelNumber, const char* carColor, int carMaxSpeed)
	{
		wheels = wheelNumber;
		color = carColor;
		maxSpeed = carMaxSpeed;
	}
}; 
```

Here the constructor takes three parameters, a variable for how many wheels the car gets, the color, and the max speed of the car, then it sets the equivalent variables to the ones given.

The code block below shows how you could use it:

```cpp
class Car
{
public:
	int wheels;
	std::string color;
	int maxSpeed;
	
	Car(const int wheelNumber, const char* carColor, const int carMaxSpeed)
	{
		wheels = wheelNumber;
		color = carColor;
		maxSpeed = carMaxSpeed;
	}
}; 

int main()
{
	Car car1(4, "black", 200);
	
	std::cout << car1.color << std::endl;
}
```

```output
black
```

#### Destructors
Destructors are the exact same as a constructor, but instead of running while the object is initialized, it runs before it gets destroyed. To write a destructor, you type the symbol `~` before the class name like so:
```cpp
class Car
{
public:
	~Car()
	{
		std::cout << "Car class has been destroyed" << std::endl;
	}
};
```

Here, the class will print `"Car class has been destroyed"` when the class goes out of scope or gets deleted.

#### Member initializer lists
A member initializer list is a better way to initialize variables in a class. Instead of first declaring the variable, and then defining that variable later in the constructor. Which takes time and recourses from your computer. You can define the variables as they are being created.

To do this, write a colon after your constructor, then the name of the variable you want to define, then you define the variable in a set of parentheses. Here is the previous example to show this:
```cpp
class Car
{
public:
	int wheels;
	std::string color;
	int maxSpeed;
	
	Car(const int wheelNumber, const char* carColor, const int carMaxSpeed)
	{
		wheels = wheelNumber;
		color = carColor;
		maxSpeed = carMaxSpeed;
	}
}; 
```

Instead of the code above, you can write it like this:
```cpp
class Car
{
public:
	int wheels;
	std::string color;
	int maxSpeed;
	
	Car(const int wheelNumber, const char* carColor, const int carMaxSpeed)
		: wheels(wheelNumber), color(carColor), maxSpeed(carMaxSpeed)
	{
	
	}
}; 
```
Here it is important to note that the variables are defined in the same order as they are declared.
If written in the wrong order, you may get errors. 


### Visibility


## Other types of classes


### [[Structs in c++]]

In a few words, a struct is a class that as a standard has its methods and members public. While all a class's methods and members are private, if not specified otherwise.
However, structs are very rarely used this way, and are most often used to represent a dataset. Like a vector 2, or coordinates.


### [[Interfaces in c++]]

Interfaces are like class blueprints that other classes can inherit from, so if a new class inherits from the interface, it has to include all the methods the interface has. These functions can then be overwritten.

### [[Enums in c++]]
