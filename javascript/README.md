# JavaScript

## How to print values to the console

The console is a tool that developers use to record the output of their JavaScript programs.

The `console.log()` command is used to print -- or "log" -- text to the console.

```
console.log("Hello " + "world!");  // Prints "Hello world!"
console.log(3+7);  // Prints "10"
console.log(3===4);  // Prints "false"

let my_object = {a: 1, b:2};
console.log(my_object);  // Prints "{a: 1, b:2}"

let a = "b";
console.log(a);  // Prints "b"

let my_number_array = [1, 2, 3, 4];
let my_string_array = ["x", "y", "z"];
console.log(my_number_array);  // Prints "[1, 2, 3, 4]"
console.log(my_string_array);  // Prints "['x', 'y', 'z']"
console.log(2/0);  // Prints "Infinity"

let n;
console.log(n);  // Prints "undefined"
```

## Data Types

Data types are the building blocks of all languages and essential pieces of any program.

Below are examples of four *primitive* data types that lay the foundation for all JavaScript programs. Primitive data types, as their name implies, are the simplest built-in forms of data.

```
console.log('New York City');
console.log(40.7);
console.log(true);
console.log(null);
```

In the example above, the computer logs each of the four *primitive* data types to the console. The types include:

* Strings — Any grouping of keyboard characters (letters, spaces, numbers, or symbols) surrounded by single quotes ('Hello') or double quotes ("World!"). In the example above, 'New York City' is a string.
* Numbers — Any number, including numbers with decimals: 4, 1516, .002, 23.42. In the example above, 40.7 is a number.
* Booleans — Either true or false, with no quotations. In the example above, true is a boolean.
* Null — Can only be null. It represents the absence of value.

## Math Operators

Math doesn't need to be your strong suit to learn JavaScript. However, there are operators you'll need to know to make useful programs.

JavaScript supports the following math operators:

* Add: +
* Subtract: -
* Multiply: *
* Divide: /

These all work how you might guess:

```
console.log(3 + 4); // Equals 7
console.log(5 - 1); // Equals 4
console.log(4 * 2); // Equals 8
console.log(9 / 3); // Equals 3
```

In the example above, each line uses a different mathematical operator to log a value to the console.

## Properties

When you introduce a new piece of data into a JavaScript program, the browser saves it as an *instance* of the data type. An instance is an individual case (or object) of a data type.

JavaScript will save a new piece of data, like 'Hello', as a string instance in the computer's memory. Another example, the number 40.7, is stored as an instance of the number data type.

An instance, like the string 'Hello', has additional information attached to it.

For example, every string instance has a property called `length` that stores the number of characters in it. You can retrieve property information by appending the string with a period and the property name:

```
console.log('Hello'.length);
```

In the example above, the value saved to the length property is retrieved from the string, 'Hello'. The program prints 5 to the console, because Hello has five characters in it.

## Built-in Methods

While the length of a string is calculated when an instance is created, a string instance also has *methods* that calculate new information as needed. When these built-in methods are called on an instance, they perform actions that generate an output.

Built-in methods are called, or used, by appending an instance with a period, the name of the method, and opening (() and closing ()) parentheses. Consider the examples below:

```
console.log('Hello'.toUpperCase());  // 'HELLO'
console.log('Hey'.startsWith('H'));  // true
```

Let's look at each line separately:

* On the first line, the .toUpperCase() method is called on the string instance 'Hello'. The result is logged to the console. This method returns a string in all capital letters: 'HELLO'.

* On the second line, the .startsWith() method is called on the string instance "Hey". This method also accepts the character 'H' as an input between the opening and closing parentheses. Since the string 'Hey' does start with the letter 'H', the method returns the boolean true.

You can find a list of built-in string methods in the [JavaScript documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/prototype). Developers use documentation as a reference tool. It describes JavaScript's keywords, methods, and syntax.

## Libraries

Instance methods, by definition, require that you create an instance before you can use them. What if you want to call a method without an instance? That's where JavaScript libraries come in. Libraries contain methods that you can call without creating an instance.

One such collection contains mathematical methods, aptly named the `Math` library.

Let's see how you call the `.random()` method from the `Math` library:

```
console.log(Math.random()); // random number between 0 and 1
```

In the example above, we called the `.random()` method by appending the library name with a period, the name of the method, and opening (() and closing ()) parentheses. This method returns a random number between 0 and 1. This code prints a random number between 0 and 1.

To generate a random number between 0 and 50, we could multiply this result by 50, like so:

```
Math.random() * 50;
```

The answer in the example above will most likely be a decimal. To ensure the answer is a whole number, JavaScript provides a built-in method called `Math.floor()`. `Math.floor()` takes a decimal number, and rounds down to the nearest whole number. You can use `Math.floor()` to round a random number like this:

```
Math.floor(Math.random() * 50);
```

In this case:

1. `Math.random` generates a random number between 0 and 1.
2. Multiply that number by 50, so now we have a number between 0 and 50.
3. `Math.floor` rounds the number down to the nearest whole number.

## Comments

As we write JavaScript, we can create comments in our code.

Programs do not evaluate comments when you run them. In other words, they exist just for human readers. Good comments are useful for you and other developers, because they describe what the code does.

There are two types of code comments in JavaScript:

* A single line comment will comment out a single line and is denoted with two forward slashes // preceding a line of JavaScript code.

```
// The first 5 decimals of pi
console.log('Pi is equal to ' + 3.14159);
```

* A multi-line comment will comment out multiple lines and is denoted with /* to begin the comment, and */ to end the comment.

```
/*
console.log('All of this code');
console.log('Is commented out');
console.log('And will not be executed);
*/
```
## Variables

Programmers use variables to write code that is easy to understand and repurpose.

Imagine you're writing a weather app. Your thermometer outside reports the temperature in Celsius, but your goal is to record the temperature in Fahrenheit.

You write a program that takes a temperature of 15 degrees Celsius and calculates the temperature in Fahrenheit.

Once you've done this though, you see the temperature now reads 16 degrees Celsius. To find Fahrenheit again, you'd need to write a whole new program to convert 16 degrees Celsius to Fahrenheit.

That's where variables come in. Variables allow us to assign data to a word and use the word to reference the data. If the data changes (like degrees Celsius) we can replace the variable's value instead of re-writing the program.

In this lesson you will learn about two ways to declare variables: `let` and `const`.

## Create a Variable: const

Let's dive in and see a variable in the wild. Here is how you declare a constant variable:

```
const myName = 'Arya';
console.log(myName);
// Output: Arya
```

Let's consider the example above:

`const`, short for constant, is a JavaScript keyword that creates a new variable with a value that cannot change.
`myName` is the variable's name. Notice that the word has no spaces, and we capitalized the N. Capitalizing in this way is a standard convention in JavaScript called camelCasing, because the capital letters look like the humps on a camel's back.
`=` is the assignment operator. It assigns the value ('Arya') to the variable (myName).
'Arya' is the value assigned (=) to the variable myName.
After the variable is declared, we can print 'Arya' to the console with: `console.log(myName)`.

You can save any data type in a variable. For example, here we save numbers:

```
const myAge = 11;
console.log(myAge);
// Output: 11
```

In the example above, on line 1 the `myAge` variable is set to 11. Below that, `console.log()` is used to print 11 to the console.

## Create a Variable: let

Constant variables, as their name implies, are constant — you cannot assign them a different value.

Let variables however, can be reassigned.

```
let meal = 'Enchiladas';
console.log(meal);
meal = 'Tacos';
console.log(meal);
// output: Enchiladas
// output: Tacos
```

In the example above, the `let` keyword is used to create the meal variable with the string 'Enchiladas' saved to it. On line three, the meal variable is changed to store the string 'Tacos'.

You may be wondering, when to use `const` vs `let`. In general, only use `const` if the value saved to a variable does not change in your program.

## Undefined

What happens if you create a variable, but don't assign it a value?

JavaScript creates space for this variable in memory and sets it to undefined. Undefined is the fifth and final primitive data type. JavaScript assigns the undefined data type to variables that are not assigned a value.

```
let whatAmI;
```

In the example above, we created the variable `whatAmI` without any value assigned to it. JavaScript creates the variable and sets it equal to the value undefined.

## Mathematical Assignment Operators

In this exercise, let's consider how we can use variables and math operators to calculate new values and assign them to a variable. Check out the example below:

```
let x = 4;
x = x + 1;
```
In the example above, we created the variable `x` with the number 4 assigned to it. On the following line, `x = x + 1` increases the value of `x` from 4 to 5.

Notice, on line two in the example above, to increment `x` by one we had to write the `x` variable on the left and right side of the assignment operator (`=`). Using a variable twice in one expression is redundant and confusing.

To address this, JavaScript has a collection of built-in mathematical assignment operators that make it easy to calculate a new value and assign it to the same variable without writing the variable twice. See examples of these operators below.

```
let x = 4;
x += 2;  // x equals 6

let y = 4;
y -= 2;  // y equals 2

let z = 4;
z *= 2;  // z equals 8

let r = 4;
r++;  // r equals 5

let t = 4;
t--;  // t equals 3
```

In the example above, operators are used to calculate a new value and assign it to the same variable. Let's consider the first three and last two operators separately:

1. The first three operators (`+=`, `-=`, and `*=`) perform the mathematical operation of the first operator (`+`, `-`, or `*`) using the number on the right, then assign the new value to the variable.
2. The last two operators are the increment (`++`) and decrement (`--`) operators. These operators are responsible for increasing and decreasing a number variable by one, respectively.

## String Interpolation

In previous exercises, we assigned strings to variables. Here, you will learn how to insert the content saved to a variable into a string.

The JavaScript term for inserting the data saved to a variable into a string is *string interpolation*.

The `+` operator, known until now as the addition operator, is used to interpolate (insert) a string variable into a string, as follows:

```
let myPet = 'armadillo';
console.log('I own a pet ' + myPet + '.'); 
// Output: 'I own a pet armadillo.'
```

In the example above, we saved the value `'armadillo'` to the `myPet` variable. On the second line, the `+` operator is used to combine three strings: `I own a pet`, the value saved to `myPet`, and `..` We log the result of this interpolation to the console as:

```
I own a pet armadillo.
```

## String Interpolation II

In the newest version of JavaScript (ES6), we can insert variables into strings with ease, by doing two things:

1. Instead of using quotes around the string, use backticks (this key is usually located on the top of your keyboard, left of the 1 key).
2. Wrap your variable with `${myVariable}`, followed by a sentence. No `+`s necessary.

ES6 string interpolation is easier than the method you used last exercise. With ES6 interpolation we can insert variables directly into our text.

It looks like this:

```
let myPet = 'armadillo'
console.log(`I own a pet ${myPet}.`)
// Output: 'I own a pet armadillo.'
```

In the example above, the backticks (\`) wrap the entire string. The variable (`myPet`) is inserted using `${}`. The resulting string is:

```
I own a pet armadillo.
```
