# Python

## script.py file

### Print to the console
```
print("Welcome to Python!")
```
### Declaring and initializing variables

```
# Declare and initialize a variable
my_variable = 10

# Print the variable to the console
print(my_variable)
```
### Booleans

```
a = True
b = False
```

```
# Set the variables
my_int = 7
my_float = 1.23
my_bool = True

# Print the variables
print(my_int)
print(my_float)
print(my_bool)
```

### Reassigning variables

```
# my_int is set to 7 below. What do you think
# will happen if we reset it to 3 and print the result?

my_int = 7

# Change the value of my_int to 3

my_int = 3

# Here's some code that will print my_int to the console:

print(my_int)
```

### Whitespace

In Python, whitespace is used to structure code. Whitespace is important, so you have to be careful with how you use it.

Bad format:
```
def spam():
eggs = 12
return eggs
        
print(spam())
```

### Whitespace Means Right Space

Now let's examine the error from the last section:

```
IndentationError: expected an indented block
```

You'll get this error whenever your whitespace is off.

We will use two-space indentation (two blank spaces for each indentation) to make sure you can easily read code with multiple indentations in your browser. You will also see Python code that uses four-space indentation. Both are correct, as long as you make sure to be consistent throughout your code.

Good format:
```
def spam():
  eggs = 12
  return eggs
        
print(spam())
```

### The Interpreter

The interpreter runs your code line by line, and checks for any errors.

```
cats = 3
```

In the above example, we create a variable cats and assign it the value of 3.

### Single Line Comments

You probably saw us use the # sign a few times in earlier exercises. The # sign is for comments. A comment is a line of text that Python won't try to run as code. It's just for humans to read.

Comments make your program easier to understand. When you look back at your code or others want to collaborate with you, they can read your comments and easily figure out what your code does.

### Multi-Line Comments

The # sign will only comment out a single line. While you could write a multi-line comment, starting each line with #, that can be a pain.

Instead, for multi-line comments, you can include the whole block in a set of triple quotation marks:

```
"""
Sipping from your cup 'til it runneth over,
Holy Grail.
"""
```
### Math

Great! Now let's do some math. You can add, subtract, multiply, and divide numbers like this:

```
addition = 72 + 23
subtraction = 108 - 204
multiplication = 108 * 0.5
division = 108 / 9
```

### Exponentiation

All that math can be done on a calculator, so why use Python? Because you can combine math with other data types (e.g. booleans) and commands to create useful programs. Calculators just stick to numbers.

Now let's work with exponents.

```
eight = 2 ** 3
```

In the above example, we create a new variable called eight and set it to 8, or the result of 2 to the power of 3 (2^3).

Notice that we use ** instead of * or the multiplication operator.

### Modulo

Our final operator is modulo. Modulo returns the remainder from a division. So, if you type 3 % 2, it will return 1, because 2 goes into 3 evenly once, with 1 left over.

```
# Set spam equal to 1 using modulo on line 3!

spam = 10%3

# Write your code above!

print(spam)
```

## The Meal

Now let's apply the concepts from the previous section to a real world example.

You've finished eating at a restaurant, and received this bill:

* Cost of meal: $44.50
* Restaurant tax: 6.75%
* Tip: 15%

You'll apply the tip to the overall cost of the meal (including tax).

## The Tax

Now let's create a variable for the tax percentage.

The tax on your receipt is 6.75%. You'll have to divide 6.75 by 100 in order to get the decimal form of the percentage. (See the Hint if you would like further explanation.)

You'll apply the tip to the overall cost of the meal (including tax).
