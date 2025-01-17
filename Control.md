
# Conditional

```Python
def branches(x):
  if x > 5:
    print ("x > 5")
  elif x == 5:
    print ("x = 5")
  else:
    print ("x < 5")
```

Note the difference between these two programs.

### Program #1

```Python
def branches(x):
  if x > 5:
    print ("x > 5")
  elif x == 5:
    print ("x = 5")
  elif x == 5:
    print ("blah")
  else:
    print ("x < 5")
```

### Program #2:

```Python
def branches(x):
  if x > 5:
    print ("x > 5")
  elif x == 5:
    print ("blah")
  elif x == 5:
    print ("x = 5")
  else:
    print ("x < 5")
```

# Exercise Fizzbuzz

# While Loop

```Python
def printList(xs):
  for i in range(0, len(xs)):
    print(xs[i])
```

# Exercise Out of Bounds access

```Python
xs = [1, 2, 3]

def safeIndex(xs, i):
    if i < 0 or i > len(xs):
        return None 
    else:
        return xs[i]

print(safeIndex(xs, 4))
```

Bubble sort

```Python
def sort(xs):
    cont = True
    n = len(xs)

    while cont:
        cont = False 

        for i in range(0, n - 1):
            x = xs[i]
            y = xs[i + 1]

            if x > y:
                xs[i] = y
                xs[i + 1] = x
                cont = True

    return xs


print(sort([-300, 1, 88, 6, 12, 10, -5, 17]))
```
