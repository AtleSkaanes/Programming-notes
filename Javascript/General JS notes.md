`JavaScript` is a language is a dynamically typed high level programming language, which basically means that it automatically assigns types to variables, and that it is more readable for humans than languages like `c++` (see [[General c++ notes]]), however, it is harder for computers to read, so programs are slower.

It is a newer language, being introduced in 1995 by Brendan Eich.

#### Extern notes
> [[General c++ notes]]
> [[Variables in JS]]


## Basics

### Basic setup

Unlike `c++` and `c#`, `JavaScript` doesn't have a specific function or class that you need to have your code in for it to run. You can just type your code anywhere in the empty document, like this:

```js
let a = 5;
let b = 6;

console.log(a + b);
```

```output
11
```

As you can see in the code above, we created two variables `a` and `b`, and the way we did that was with the `let` keyword. We also used `console.log()`, which is the way that `javaScript` outputs to the console.

## Variables

Variables in `JavaScript` don't need a type-name to be initialized, they do however need a keyword like `let`,  `var` or `const`.
An example of initializing a few different arrays could be:

```js
let number1 = 1;
let number2 = 2;
let number3 = number1 + number2;

let string1 = "Hello";
let string2 = " World!";
let string3 = string1 + string2;

console.log(number3);
console.log(string3);
```

```output
3
Hello World!
```

Not only did we 