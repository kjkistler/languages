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
