
# Reading 

These notes cover the second lecture and are over sections [1.3.X](https://www.composingprograms.com/pages/13-defining-new-functions.html) "Defining New Functions" and 
[1.4.X](https://www.composingprograms.com/pages/14-designing-functions.html) "Designing Functions" of the textbook - [Composing Programs](https://www.composingprograms.com/).

# Environments

Recall from section [1.2.4 "Names and the Environment"](https://www.composingprograms.com/pages/12-elements-of-programming.html#names-and-the-environment) that in Python, the _evaluation environment_ or _environment_ refers to a collection of _variables_ along with the _bindings_ for those variables. A variable is an _identifier_ (or name) beginning with a capital or lowercase alphabetical character followed by an arbitrary sequence of alphabetical, numeric, or underscore characters. The identitifers `myVar`, `x1`, `debounce`, and `state_1` are all examples of valid names for variables; however, by convention I will write all variable names in [camel case](https://en.wikipedia.org/wiki/Camel_case). A _variable binding_ is the value that is _bound_ to a given variable, so for example in the following Python code we have variables `x1`, `x2`, and `x3` along with the respective bindings `10`, `"hello world"`, and `True`.

## Environment Examples

```python
x1 = 10
x2 = "hello world"
x3 = True
```

You should imagine the _environment_ with these bindings as something similar to a dictionary containing entries for `x1`, `x2`, `x3` with the associated "definitions" `10`, `"hello world"`, and `True`, that is:

| Variable | Binding         |
| -------- | --------------- |
| `x1`     | `10`            |
| `x2`     | `"hello world"` |
| `x3`     | `True`          |

In this code we modify the _evaluation environment_ by binding `x1` to `10`, `x2` to `"hello world`", and `x3` to `True`. The assignment or `=` operator is just one way of introducing new _bindings_ into the environment. As is in the case in many modern programming languages, Python supports modules and syntactic sugar in the form of function statements that can also be used to introduce new bindings into the _environment_. 

# Statements

Statements are another part of Python's syntax. Statements are made up of zero or more keywords, reserved symbols, or expressions.

## Assignment statements 

We are already familiar with assignment statements from the previous sections. Assignment statements are of the form (replacing `<variable name>` with a valid Python identifier, and replacing `<expression>` with a valid Python expression):

```python
<variable name> = <expression>
```

The code example from the [environment section of these notes](#environment-examples) for concrete examples of assignment statements.

## Function Statements

Recall from the previous set of notes that we can write a function as an expression using the `lambda` keyword. Further, we can define a function by assigning a variable to the `lambda` expression:

```Python
square = lambda x: x**2
```

Python provides an alternative syntax for defining _top-level_ functions through the use of function statements. Function statements are of the form:

```Python
def <identifier>(<arg 1>, <arg 2>, ...):
  <statement or expression>
  ...
```

We could rewrite the `square` function using a function statement as:

```Python
def square(x):
  # Note that we must add the "return" keyword if we want the square function to return `x**2` as an output.
  return x**2
```

### Exercise 1.

Write two versions of the `square` function called `squareV1` and `squareV2` using a function statement. For the `squareV1` function include the `return` keyword just as written above. For the `squareV2` function omit the `return` keyword. Call and print the output of these two functions and compare their results.

<details>
  <summary>Solution</summary>

  Copy the following code into a `*.py` file such as `squares.py`, but the name doesn't matter. 
  
```Python
def squareV1(x):
  return x**2

def squareV2(x):
  x**2

print(squareV1(5))
print(squareV2(5))
```

  Run the Python file in MSYS2 by copying the name of the file into MSYS2 with the `python` command prepended.

```shell
$ python path/to/file/squares.py
25
None
```

  Without the `return` keyword we can see that `squareV2` has no _return_ value and implicitly returns the value `None`.



</details> 

## Import Statements

Import statements are use to import code from other Python files into the enclosing Python file that the import appears in. Python file along with their _environments_ are known as modules. To import the [`math`](https://docs.python.org/3/library/math.html) module you can write:

```Python
import math

# will print -1
print(math.cos(math.pi))
```

The complete syntax for import statements is desribed in [section 5 "The import system" of the official Python guide](https://docs.python.org/3/tutorial/modules.html). Importing a Python module will take any bindings defined by the imported module and merge that with the current files environment. To see what I mean, consider the environment for an empty Python file.

```Python
# This is our empty Python file, call is "A.py".
```

| Variable | Binding         |
| -------- | --------------- |

If we then include an import statement `import math` the environment of the "A.py" when run will change from empty to include all of the bindings that the [`math`](https://docs.python.org/3/library/math.html) module defines.

| Variable | Binding         |
| -------- | --------------- |
| cos      | <lambda>        |
| pi       | 3.1415926...    |
| sin      | <lambda>        |
| ...      | ...             |

You can print the full global Python environment using the function [`globals`](https://docs.python.org/3/library/functions.html#globals) and the current local Python environment using [`local`](https://docs.python.org/3/library/functions.html#locals).

# Next Reading

Read sections 1.5, 1.6, and 1.7 by the 14th of Janurary. No class will be held on Jan 7th or Jan 9th.
