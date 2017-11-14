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
### The Console Object

The Console object provides access to the browser's debugging console (e.g., the Web Console in Firefox). The specifics of how it works vary from browser to browser, but there is a de facto set of features that are typically provided.

For more information, see [Console](https://developer.mozilla.org/en-US/docs/Web/API/Console).

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

## Introduction to Control Flow

In this lesson, we'll explore how we can use the building blocks of JavaScript to write programs that make decisions.

Control flow statements enable JavaScript programs to make decisions by executing code based on a condition. If a given condition is true, we execute one block of code. If the statement is false, we execute another block of code. For instance, if we were making a game in which the user had to choose which door to enter, we'd need a way for the program to know what to do once the user was in the next room.

In this lesson, we'll learn how to make decisions with JavaScript and how it can control the program's flow.

## if/else Statements

The core task of programming is writing lists of instructions for computers, or translating our ideas from human-speak to computer-speak.

Let's learn how we can ask JavaScript to think like us and make decisions the way we do.

We'll start with human-speak. Many decisions we make everyday boil down to this sentence in some form:

"If something is true, let's do option 1, or else, if it is false, let's do option 2."

This sentence looks fairly similar when we write it with JavaScript. See for yourself:

```
let needsCoffee = true;
if (needsCoffee === true) {
    console.log('Finding coffee');
} else {
    console.log('Keep on keeping on!');
}
```

1. Lines of code between curly braces are called blocks. if/else statements have two code blocks. If the variable `needsCoffee` is true, the program will run the first block of code. Otherwise, it will run the other block of code.

2. `needsCoffee` is the condition we are checking inside the `if`'s parentheses. Since it is equal to true, our program will run the code between the first opening curly brace `{` (line 2) and the first closing curly brace `}` (line 4). It will ignore the else `{ ... }` part. In this case, we'd see `Finding coffee` log to the console.

3. If `needsCoffee` were false, only the `console.log()` statement in the else block would be executed.

if/else statements are how programs can process yes/no questions programmatically.

## True and False Values

In the previous exercise, we wrote if/else statements. If a given condition were true, one block of code would run. If that condition were false, a different block of code would run. However, there are data types that are not booleans. Let's explore the concepts of true and false in variables that contain other data types, including strings and numbers.

In JavaScript, all variables and conditions have a truthy or falsy value.

```
let variableOne = 'I Exist!';
if (variableOne) {
// This code will run because variableOne contains a truthy value.
} else {
// This code will not run because the first block ran.
}
```

In the first line of the program above, a variable is created and set. The value of this variable is a string rather than a boolean. How does this program determine which code block to run?

The second line of this program checks a condition `if (variableOne)`. In the previous exercise, we checked if a variable was equal to true or false. By only writing the name of the variable as the condition, we are checking the *truthiness* of `variableOne`. In this case, `variableOne` contains a truthy value.

If we changed `if (variableOne)` to, say, `if (variableTwo)`, that condition would evaluate to falsy because we have not created a variable called `variableTwo` in this program. In other words, `variableOne` is truthy and `variableTwo` is falsy.

All variables that have been created and set are truthy (and will evaluate to true if they are the condition of a control flow statement) unless they contain one of the seven values listed below:

* false
* 0 and -0
* "" and '' (empty strings)
* null
* undefined
* NaN (Not a Number)
* document.all (something you will rarely encounter)

There is an important distinction between a variable's value and its truthiness: `variableOne`'s value is `'I exist'` because that is the data saved to the variable. `variableOne` is truthy because it exists and does not contain any of the seven falsy values listed above.

## True and False Values II

In programming, we often evaluate whether or not an expression is true or truthy. Conveniently, JavaScript provides a shorthand notation for this.

```
let isRaining = true;
if (isRaining) {
   console.log('Carry an umbrella!');
} else {
  console.log('Enjoy the sun!');
}
```

In the example above, the condition is simply if `(isRaining)`. In JavaScript, this is evaluating whether `isRaining` is truthy. If you read the code out loud to yourself, it sounds like a simple sentence: "If it's raining, carry an umbrella. Else, enjoy the sun!"

JavaScript provides an operator for swapping the truthiness and falsiness of values - the exclamation point (`!`). We can use this in conditional statements as shorthand to check if the value of a variable evaluates to false rather than true.

```
let isPhoneCharged = true; 
if (!isPhoneCharged) {
  console.log('Plug in your phone!');
} else {
  console.log('No need to charge!');
}
```

In the example above, the program checks if `isPhoneCharged` evaluates to false. Because `isPhoneCharged` is true, the second block of code will execute.

## Comparison Operators

In addition to checking whether a variable evaluates to true or false, sometimes we need to compare variables to other values. We can achieve this with *comparison operators*.

There are two comparisons you might be familiar with:

* Less than: `<`
* Greater than: `>`

You may also recognize these:

* Less than or equal to: `<=`
* Greater than or equal to: `>=`

These comparisons evaluate to true or false.

## Comparison Operators II

There are two more useful comparisons we can make. Often, we might want to check if two things are equal to each other or if they are not.

1. To check if two things equal each other, we write `===` (three = signs in a row).
2. To check if two things do not equal each other, we write `!==` (an exclamation point with two = signs in a row).

It can be confusing when to use one `=` sign and when to use three `===` signs. Use a single `=` to assign a value to a variable. Use `===` to compare the values of two different variables.

## else if Statements

We've explored if/else statements that answer questions that are either yes or no. What can we do if we have a question that has multiple yes conditions, or multiple no conditions?

We can add more conditions to our if/else statement with else if. Check out how this fits into our current knowledge of if/else statements:

```
let stopLight = 'green';

if (stopLight === 'red') {
  console.log('Stop');
} else if (stopLight === 'yellow') {
  console.log('Slow down');
} else if (stopLight === 'green') {
  console.log('Go!');
} else {
  console.log('Caution, unknown!');
}
```

1. We created a variable named `stopLight` that is assigned to the string `"green"`.

2. Then, there's an if/else statement with multiple conditions, using `else if`. `else if` allows us to check multiple values of the `stopLight` variable and output different things based on its color.

3. The block ends with the singular `else` we have seen before. The `else` is a catch-all for any other situation. For instance, if `stopLight` were blinking blue, the last `else` would catch it and return a default message.

## Logical Operators

We can translate certain thoughts into JavaScript code such as, "Are these things equal?" with `===`, or, "Is one thing greater than another thing?" with `>`.

In English, sometimes we say "both of these things" or "either one of these things." Let's translate those phrases into JavaScript with special operators called *logical operators*.

1. To say "both must be true," we use `&&`.
2. To say "either can be true," we use `||`.

For example:

```
if (stopLight === 'green' && pedestrians === false) {
  console.log('Go!');
} else {
  console.log('Stop');
}
```

In the example above, we make sure that `stopLight` is `'green'` and (`&&`) there are no pedestrians before we log `'Go!'`.
If either of those conditions is false, we log `'Stop'`.

Just like the operators we learned previously, these logical operators will return either true or false.

These logical operators are helpful when writing if/else statements since they let us make sure multiple variables are true or false. We can combine these operators with all of the ones we have learned throughout this lesson.

## switch Statements

Before we move on, let's circle back to `else if` statements.

Using `else if` is a great tool for when we have a few different conditions we'd like to consider.

`else if` is limited, however. If we want to write a program with 25 different conditions, like a JavaScript cash register, we'd have to write a lot of code, and it can be difficult to read and understand.

To deal with times when you need many `else if` conditions, we can turn to a `switch` statement to write more concise and readable code.

To a computer, a `switch` statement and an `if`/`else` statement are the same, but a `switch` statement can be easier for humans to read. Part of being a good developer is writing code that both computers and humans can read.

`switch` statements look like this:

```
let groceryItem = 'papaya';

switch (groceryItem) {
  case 'tomato':
    console.log('Tomatoes are $0.49');
    break;
  case 'lime':
    console.log('Limes are $1.49');
    break;
  case 'papaya':
    console.log('Papayas are $1.29');
    break;
  default:
    console.log('Invalid item');
    break;
}
```

1. The `switch` keyword initiates the statement and is followed by `()`, which contains the condition that each case will compare to. In the example, the condition is `groceryItem`.

2. Inside the block, `{}`, there are `case`s. `case` is like the `else if` part of an `if`/`else if`/`else` sequence. The word following the first case is `'tomato'`. If `groceryItem` equalled `'tomato'`, that `case`'s `console.log()` would run.

3. `groceryItem` equals `'papaya'`, so the first and second `case` statements are skipped. The third `case` runs since the `case` is `'papaya'`, which matches `groceryItem`'s value. This particular program will log `Papayas are $1.29`.

4. Then the program stops with the `break` keyword. This keyword will prevent the `switch` statement from executing any more of its code. Without adding `break` at the end of each `case`, the program will execute the code for all matching `case`s and the default code as well. This behavior is different from `if`/`else` conditional statements, which execute only one block of code.

5. At the end of each `switch` statement, there is a default condition. If none of the cases are true, then this code will run.

## Ternary Operator

In the previous exercise, we learned shorthand for writing multiple `if`/`else if`/`else` statements to make them easier to read. JavaScript also provides a way to shorten simple `if`/`else` statements called the *ternary operator*.

```
let isNightTime = true;

if (isNightTime) {
  console.log('Turn on the lights!');
} else {
  console.log('Turn off the lights!');
}
```

In the example above, we see a very familiar pattern. See the example below for an equivalent way to express this.

```
isNightTime ? console.log('Turn on the lights!') : console.log('Turn off the lights!');
```

The code in the example above will operate exactly as the code from the previous example. Let's break this example into its parts:

1. `isNightTime ?` — the conditional statement followed by a question mark. This checks if `isNightTime` is truthy.

2. `console.log ('Turn on the lights!')` — this code will be executed if the condition is truthy.

3. `:` — a colon separates the two different blocks of code that can be executed.

4. `console.log('Turn off the lights!');` — this code will be executed if the condition is falsy

In this example, we checked if the value of a variable was true or false. The ternary operator can be used for any condition that can be evaluated to true or false, such as those with comparison operators.

```
age >= 16 ? console.log('You are old enough to drive in the United States!') : console.log('You are not old enough to drive in the United States!');
```

In the example above, the conditional statement is checking whether the value of the variable `age` is greater than or equal to `16`. If so, a message that states the user is old enough to drive will be logged to the console. Otherwise, a message that states the user is not old enough to drive will be logged.
