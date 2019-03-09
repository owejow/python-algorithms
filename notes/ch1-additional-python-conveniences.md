# Additinal Python Conveniences

Useful python functionality for writing clear and consice code.


### Conditional Expressions

**conditional expressions**: replace simple control structures

```python
expr1 if condition else expr2
```
Evaluate expr1 if condition is True otherwise expr2. Similar to ternary operator in 
C:

```c
condition ? expr : expr2
```

example usage:

```python
param = n if n >= 0 else -n
result = foo(param)

# more succinct
result = foo(n if n >= 0 else -n)

```

Advice: only use when conditional expressions improve readability of code

### Comprehension Syntax

**comprehension syntax**: produce one series based on evaluation of another series

**list comprehension**: generate a new list based on evaluating another sequence

```python
[expression for value in iterable if condition]

# above same as
result = []
for value in iterable:
	if condition:
		result.append(expresion)
```

Example generating squares of numbers:

```python
squares = [k*k for k in range(1, n+1)]
```

Additional comprehension syntaxes:

```python
# list comprehension
[k*k for k in range(1, n+1)]

# set comprehension
{k*k for k in range(1, n+1)}

# generator comprehension
(k*k for k in range(1, n+1))

# dictionary comprehension
{k: k*k for k in range(1, n+1)}

```

**generator comprehension**: results do not have to be stored in memory
  * can feed list comprehension directly to function

```python
# Note the generator does not require an extra set of parens
total = sum(k*k for k in range(1, n+1))
```

### Packing and Unpacking Sequences

**automatic-packing-of-tuple**:  Series of **comma-separated** expressions are given in a larger context, they are treated as a single tuple EVEN if no enclosing parentheses provided

```python
# expression treats as if tuple provided to data
data = 2, 3, 6, 8
```

**unpack** a sequence: allows assignment of individual identifiers to elements of a sequence

```python
# a=7, b=8, c=9, d=10
a, b, c, d = range(7, 11)
```

**iterables** can be used in unpacking; so long as number of variables on the left-hand side is same as number of elements in the iteration


```python
# unpack return values for a function
quotient, remainder = divmod(a, b)
```

```python
# useful in context of for loop when iterating through a sequence of iterables
for x, y in [(7,2), (5,8), (6,4)]
```

### Simultaneous Assignment

**simultaneous-assignment**: explicitly assign series of values to a series of identifiers

```pythoa
# right hand side automatically packed to a tuple and then automatically unpacked
x, y, z = 6, 2, 5
```

```python
# all expressions on right hand side evaluated before any of 
# the assignments in the  left hand side
j, k = k, j

# equivalent to
temp = j
j = k
k = temp
```

Simultaneous assignment the right hand side tuple serves as the temporary variable

```python
# swapping simplifies presentation of the code
def fibonacci():
	a, b = 0, 1
    while True:
    	yield a
        a, b = b, a+b
```