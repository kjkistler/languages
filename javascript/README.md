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

