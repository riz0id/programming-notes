
# Reading 

These notes cover the second lecture and are over sections [1.3.X](https://www.composingprograms.com/pages/13-defining-new-functions.html) "Defining New Functions" and 
[1.4.X](https://www.composingprograms.com/pages/14-designing-functions.html) "Designing Functions" of the textbook - [Composing Programs](https://www.composingprograms.com/).

# Environments 

Recall from section [1.2.4 "Names and the Environment"](https://www.composingprograms.com/pages/12-elements-of-programming.html#names-and-the-environment) that in Python, the _evaluation environment_ or _environment_ refers to a collection of _variables_ along with the _bindings_ for those variables. A variable is an _identifier_ (or name) beginning with a capital or lowercase alphabetical character followed by an arbitrary sequence of alphabetical, numeric, or underscore characters. The identitifers `myVar`, `x1`, `debounce`, and `state_1` are all examples of valid names for variables; however, by convention I will write all variable names in [camel case](https://en.wikipedia.org/wiki/Camel_case). A _variable binding_ is the value that is _bound_ to a given variable, so for example in the following Python code we have variables `x1`, `x2`, and `x3` along with the respective bindings `10`, `"hello world"`, and `True`.

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

# Exercises 
