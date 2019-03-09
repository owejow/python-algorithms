# Modules and import statements

**130-150 functions and classes** that are defined within Python's built-in namespace

**modules**: how values and functions in standard Python distribution are organized

**imported**: how modules can be used within a program

**import**: loads defintions from a module into the current namespace

```python
# pi and sqrt are aded to current namespace
from math import pi, sqrt
```

**importing many definitions**: used import \* sytax

```python
from math import *
```
==Caution== Use import \* sparingly as it can cause unexpected name collision


Access many definitions from the same module by importing module itself:

```python
# all exported methods in math are available through math identifier
import math

math.pi
math.sqrt(2)
```


### Creating a New Module

Add defintions in file named with ".py" suffix

Example:
  * place count fucntion into file named utility.py

```python
from utility import count
```

topo-level comamnds with the module source code are executed when module is first loaded

Use special syntax to embed commands within module that will be executed if module is
directly invoked as a script, but not when the module is imorted from another script.

```python
if __name__ == '__main__':
	# module invoked as script only commands
    # these commands will not be executed if module is imported
    pass
```

### Important Existing Modules

| Module Name | Description |
|--------|--------|
| array       |  provides compact array storage for primitive types |
| collections |  additional data structures that involve collection of objects |
| copy | functions for making copies of objects |
| heapq | heap-based priority queue functions |
| math | common mathematical functions |
| os | support for interaction with operating system |
| random | random number generation |
| re | regular expression processing |
| sys | additional interaction methods with python interpreter |
| time | support for measuring time, or delaying a program |


### Pseudo-Random Number Generation

**pseudo-random number generator** generates numbers that are statistically random
but not necessarily truly random
  * deterministic formula that generate sthe next number in a sequence
  * Mersenne twister: technique used by Python to generate random numbers
  * next number in pseudo random number generator is deterministic

| Syntax | Description |
|--------|--------|
|  seed(hashable) |  initializes pseudo-random number generator based on hash value of parameter      |
| random() | pseudo-random floating point between [0.0, 1.0) |
| randint(a,b) | pseudo-random integer in closed interval [a, b]|
| randrange(start,stop,step)| random integer in standard python range specified by parameters |
|choice(seq)| returns element of a given sequence chosen randomly |
|shuffle(seq) | reorders elements of a given sequence pseudo-randomly |