
# Questions

## In the terminal (MSYS2) I see the three arrows (that is, `>>> `) and it turns into three dots. How do I escape that?

Seeing three arrows in terminal happens after invoking the `python` command. The three arrows are printed as a part of the Python interpreter. These arrow will turn into three dots/periods (that is, `... `) after pressing enter with a backslash `\` character as the final character of the line. The backslash character is used to break the current line without releasing the current input expression to the Python interpreter.

```shell
Jake@DESKTOP-3NQMA28 MSYS ~
$ python
Python 3.12.7 (main, Oct  3 2024, 09:03:54) [GCC 13.3.0] on cygwin
Type "help", "copyright", "credits" or "license" for more information.
>>> \
...
```

This is effectively like inserting a newline character (that is, the `\n` character on MacOS and Linux or the string `\r\n`) into the REPL for situations in which a line break is necessary without pressing the ENTER key like we typically would to insert a new line. Since this is just a continuation of the input, we can break away by simply pressing the ENTER key.
