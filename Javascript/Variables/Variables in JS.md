
#### Extern notes
> [[Strings in JS]]
> [[Arrays in JS]]
> [[Objects in JS]]


### Types
As previously mentioned, `JavaScript` is a dynamically typed language, so you don't have to declare what `type` a variable has. Therefore, there are only a few variable types that you need to know about.


| Variable | Example                  | Note              |
| -------- | ------------------------ | ----------------- |
| Number   | 5, 2.4, 10               |                   | 
| String   | "Hello World!", "35"     | [[Strings in JS]] |
| Array    | [5,2,6], ["this","that"] | [[Arrays in JS]]  |

### Keywords

Beside types, you can get different variables depending on the keyword you choose to initialize it with.
There are 3 variable keywords:

| Keyword | Usage                                                                          | When were/is it used |
| ------- | ------------------------------------------------------------------------------ | -------------------- |
| let     | To declare a variable that can change, **isn't** supported in older browsers   | 2015 - present       |
| const   | To declare a variable that can't change, **isn't** supported in older browsers | 2015 - present       | 
| Var     | Old way to declare a variable, **is** supported in older browsers              | 1995 - 2015          |


So if you want to declare a variable that you should be able to change, then use `let`, you can still use `var`, but the modern approach is to use `let`. This is useful for counters, arrays that can change, and most other use cases for variables.

Or if you want to have a variable that remains the same, and is unable to change, use `const`. This is useful for creating constant numbers, like having PI in your script. It is also useful for getting HTML objects and putting into a variable.

```js
let counter = 0;

counter = counter + 1;

console.log(counter);


const PI = 3.14;

PI = PI + 1;

console.log(PI);
```

```Output
1
TypeError: Assignment to constant variable.
```

As you can see here, we successfully changed the `counter` variable, but we got an error when we tried to change the const  `PI` variable, since it was a constant.
Refer to [[Const keyword in JS]] for more information about it.







$$0,06=\frac{\pi}{6}\cdot h^2 \cdot (6x-2h)$$

$$0,06=\frac{\pi}{6}\cdot 6xh^2-2h)$$