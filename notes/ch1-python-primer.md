# Python Studies

## Chapter 1: Python Primer

- [Python Studies](#python-studies)
  - [Chapter 1: Python Primer](#chapter-1-python-primer)
    - [Objects In Python](#objects-in-python)
      - [Identifiers](#identifiers)
      - [Reserved words](#reserved-words)
    - [Built-in class Types](#built-in-class-types)
      - [**bool**](#bool)
      - [**int**](#int)
      - [**float**: sole floating point](#float-sole-floating-point)
      - [sequence types](#sequence-types)
        - [**list**: stores sequence of objects](#list-stores-sequence-of-objects)
        - [**tuple**: immutable version of a sequence](#tuple-immutable-version-of-a-sequence)
        - [**string**: str class stores immutable sequence of characters](#string-str-class-stores-immutable-sequence-of-characters)
        - [**set**: collection of elements without duplicates](#set-collection-of-elements-without-duplicates)
          - [**frozenset**: * immutable collection of elements without duplicates](#frozenset--immutable-collection-of-elements-without-duplicates)
          - [**dict class**: dictionary or mapping for set of distinct keys to values](#dict-class-dictionary-or-mapping-for-set-of-distinct-keys-to-values)
    - [Iterables and Generators](#iterables-and-generators)
    - [Generators](#generators)
    - [Expressions Operators and Precedence](#expressions-operators-and-precedence)
      - [Logical Operators](#logical-operators)
      - [Equality Operators](#equality-operators)
      - [Comparison Operators](#comparison-operators)
      - [Arithmetic Operators](#arithmetic-operators)
      - [Bitwise Operator](#bitwise-operator)
      - [**Sequence Operators**](#sequence-operators)
      - [sets and frozensets](#sets-and-frozensets)
      - [dictionaries](#dictionaries)
      - [Extended Assignment Operators](#extended-assignment-operators)
      - [chained assignment](#chained-assignment)
      - [chaining comparison](#chaining-comparison)
      - [Control Flow](#control-flow)
      - [While Loops](#while-loops)
      - [For Loops](#for-loops)
      - [Index-Based For Loops](#index-based-for-loops)
      - [Break Statements](#break-statements)
      - [Continue Statements](#continue-statements)
    - [Functions](#functions)
      - [Information Passing](#information-passing)
      - [Mutable Parameters](#mutable-parameters)
      - [Default Parameter Values](#default-parameter-values)
      - [Keyword Parameters](#keyword-parameters)
      - [built-in functions](#built-in-functions)
    - [Simple Input and Output](#simple-input-and-output)
      - [console input and output](#console-input-and-output)
      - [input function](#input-function)
      - [Files](#files)
      - [Exception Handling](#exception-handling)
      - [Common Exception Types](#common-exception-types)
      - [Raising an exception](#raising-an-exception)
      - [Exception Handling Checking](#exception-handling-checking)
      - [catching an exception](#catching-an-exception)
      - [Exception Guidance](#exception-guidance)
    - [Modules and import statements](#modules-and-import-statements)
      - [Creating a New Module](#creating-a-new-module)
      - [Important Existing Modules](#important-existing-modules)
      - [Pseudo-Random Number Generation](#pseudo-random-number-generation)
    - [Scopes and Namespacea](#scopes-and-namespacea)
      - [Functions to examine namespace](#functions-to-examine-namespace)
      - [First-Class objects](#first-class-objects)
    - [Additional Python Conveniences](#additional-python-conveniences)
      - [Conditional Expressions](#conditional-expressions)
        - [**conditional expressions**: replace simple control structures](#conditional-expressions-replace-simple-control-structures)
      - [Comprehension Syntax](#comprehension-syntax)
        - [**list comprehension**: generate a new list based on evaluating another sequence](#list-comprehension-generate-a-new-list-based-on-evaluating-another-sequence)
        - [**generator comprehension**: results do not have to be stored in memory](#generator-comprehension-results-do-not-have-to-be-stored-in-memory)
    - [Packing and Unpacking Sequences](#packing-and-unpacking-sequences)
    - [Simultaneous Assignment](#simultaneous-assignment)

### Objects In Python

#### Identifiers

- **identifiers** are:
  - case sensitive
  - aka name
  - assignment statement sets values

#### Reserved words

- can not be identifier
- list of reserved words:

```python

False None True and as assert break class continue def

del elif else from in except global is finally  if

lambda for import nonlocal not or pass raise return try

while with yield
```

- **Dynamically typed**
  - no type specified
  - alias second identifier assigned to object

- **instantiation**
  - creating a new class
  - invoke constructor:
    - Widget()
  - literal constructor:
    - temperature = 98.6
    - temperature = float(98.6)

```python
float(98.6) == 98.6
```

- **methods**
  - member function that are part of specific instance of a class
  - [4, 1, 3].sort()

```python
sample_list = [4,1,3]
sample_list.sort()
sample_list
```

```python
# method is invoked on identifier to left of dot
identifier = 2.0
identifier.is_integer()
```

- **method types**
  - mutators or update methods: change the state of object
  - accessors return information about state of object
    but do not change its state

### Built-in class Types

| class     | description                                 |
| --------- | ------------------------------------------- |
| bool      | boolean value (immutable)                   |
| int       | integer value (immutable)                   |
| float     | float value (immutable)                     |
| list      | sequence of objects (mutable)               |
| tuple     | sequence of object (immutable)              |
| str       | character string (immutable)                |
| set       | unordered set of distinct objects (mutable) |
| frozenset | set of distinct objects (immutable)         |
| dict      | dictionary (mutable)                        |

#### **bool**

- values:
  - True
  - False
- bool: constructor, returns False by default
- values to constructor determine bool return value
  - interpretation of value depends on type
    - numbers 0 return False all else True
    - lists and sequences, non-empty True, empty False

```python
bool()

bool(1)

bool(0)

bool([])

bool([0])
```

#### **int**

- represents integer values of arbitrary magnitude
- python automatically chooses the internal representation that is most suitable
  - does not have short or long like C++ or Java
- Literals
  - integer values with sign: 0, -23, 43
  - Use octal, binary, or hexadecimal
    - 0 plus b binary: 0b111
    - 0 plus o octal: 0o44
    - 0 plus x hexadecimal: 0xff
  - constructor
    - int
      - returns 0 by default
      - truncates floats to integer
        - int(3.12) => 3
      - integer strings are converted to integer
        - int('33') => 33
        - default assumes base 10
        - if base is not decimal need to specify base
          - int('33',5) => 33
        - raises TypeError if value is not convertible
          - int('hello')****int

```python
int(3.12)
int("33", 5)
```

#### **float**: sole floating point

- uses fixed precision representation similar to double in Java and C++
- literals
  - Trailing zeros are optional:
    - 4.0 can be represented as 4.
  - scientific notation
    - 6.023e23
- constructor
  - float
  - returns 0.0 by default
  - attempts to convert string as floating point value
  - raises ValueError if not convertible

```python
float(3.12)
float("33")
```

#### sequence types

- list
- tuple
- string

##### **list**: stores sequence of objects

- referential structure: stores reference to sequence of objects
- array-based sequences that are zero-indexed
- dynamically expland and contract
- constructor:
  - list()
  - produces empty list by default
  - accepts any parameter that is iterable
  - list('hello') => ['h','e','l','l','o']

```python
list() # ()
[1,2]
```

##### **tuple**: immutable version of a sequence

- can be more efficiently represented
- delimeted by parenthesis
- single element tuple: (17,)
  - (17) viewed as simple parenthesized numeric expression
- constructor:
  - tuple
  - default: returns empty tuple

```python
tuple() # ()
(1,) # (1, )
(1,2)
```

##### **string**: str class stores immutable sequence of characters

- literal:
  - single quotes: 'hello'
  - double quotes: "hello"
  - escaped quote delimiter:
    - 'Don\'t worry'
  - escaped characters
    - newline: \n
      - unicode: \u: \u20AC
    - using """ and ''' to delimit multiline
      - can embed newline naturally

```python
"""Welcome to the GPA
   calculator
"""
```

##### **set**: collection of elements without duplicates

- highly optimized for checking if element is in a set
- restrictions
  - elements not placed in particular order
  - uses hash table as data structure
  - only immutable types can be place in set
    - supports tuples but not lists
  - set of frozensets can belong to a set
- constructor
  - literal: curly braces used as delimiter for the set
    - {17} or {'red', 'green', 'blue'}
  - set() used to create empty set
    - dictionary is returned with empty curly braces
  - iterable parameters presented in constructor return
    set of distinct elements
    - set('hello') => {'h', 'e', 'o', 'l'}

```python
set() # returns set()
set('hello')  # returns {'l', 'e', 'o', 'h'}
```

###### **frozenset**: * immutable collection of elements without duplicates

- constructor:
  - frozenset() -> empty frozenset object
  - frozenset(iterable) -> frozenset object

```python
  frozenset() # returns frozenset()
  frozenset('hello') # returns frozenset({'l', 'e', 'o', 'h'})
```

###### **dict class**: dictionary or mapping for set of distinct keys to values

- almost identical to set except associated value is stored
- literal:
  - curly braces to initialize
  - {} initializes empty dictionary
  - {'ga': 'Irish', 'de': 'German'}
- constructor:
  - dict:
    - accepts mappings as a parameter and creates a new dictionary with identical association
    - key value pairs as parameters
    - dict{[('ga', 'Irish'), ('de', 'German')]}

```python
dict()  #  returns {}
dict([('ga', 'Irish'), ('de', 'German')]) # returns {'ga': 'Irish', 'de': 'German'}
{'ir': 'Iran', 'en': 'USA'}  # returns {'ir': 'Iran', 'en': 'USA'}
```

### Iterables and Generators

- **Iterator** is an object that managers iteration through a series of values

- **iterable** is an object that produces an iterator
  - instance of list is an iterable but not an iterator

```python
# for loop automates creation of an iterable
for element in iterable
```

```python
# iterator object from list using the syntax
i = iter(data)

# next item from iterator can be called using
next(i)
```

More than one **iterator** possible on a given object

- each iterator will maintain its own state of progress
- iterator does **NOT** store its own copy of list of elements it maintains current index into the original list
- **updated** contents of the list are presented if the original list is modified before the iterator reaches that element

Python functions and classes support implicit iterables

```python
# returns iterable and not list of numbers
for j in range(1000)
```

- **lazy evaluation**: in the example of range allows the execution to not set aside memory for unnecessary values. Values are created when they are required

Exmples of iterables in Python:

- *keys()*: view of all the keys
- *values()*: view of all the values
- *items()*: view of all the (key, value) pairs

### Generators

**Generators** are the most convenient technique for creating iterators

**yield** statement is executed to indicate each element of the series

```python
  def factors(n):
    for k in range(1, n+1):
      if n % k == 0:
        yield k            # keyword yield rather than return
```

&#9658; illegal to combine return and yield statements

At the **yield** statement the procedure is temporarily interrupted only resumed when value is requested

Multiple yield statements legal for generators:

```python
  def factors(n):
    k = 1
      while k * k < n:
        if n % k == 0:
          yield k
          yield n // k
          k += 1
      if k * k == n:
      yield k
```

- **Benefits**:
  - results only computed if requested
  - entire series need not reside in memory at one time

### Expressions Operators and Precedence

- expressions: combination of existing values using operators
- compound expressions: require evaluation of two or more operators
- precedence: determines order in which operators are evaluated

#### Logical Operators

| operator | description     |
| -------- | --------------- |
| not      | unary negation  |
| and      | conditional and |
| or       | conditional or  |

Note: or and and operators short-circuit

- if result can be determined based on value of first operand
- useful for constructing boolean expressions

#### Equality Operators

| operator | description                                                                                                |
| -------- | ---------------------------------------------------------------------------------------------------------- |
| is       | same identity  evaluates to True if a and b are aliases to same object                                     |
| is not   | different identity  evaluates to Trueif not aliases to same object                                         |
| ==       | equivalent evaluates to true if a nd be refer to the same or different objects that evaluate to same value |
| !=       | not equivalent                                                                                             |

#### Comparison Operators

| Operator | Description              |
| -------- | ------------------------ |
| <        | less than                |
| <=       | less than or equal to    |
| >        | greater than             |
| >=       | greater than or equal to |

Works for datatypes that have natural order:

- defined lexicograhically and case sensitively for strings
- exception raise if operands incompatible types

```python
2 > 4
"bye" < "hello"
```

#### Arithmetic Operators

| Operator | Description      |
| -------- | ---------------- |
| \+       | addition         |
| \-       | subtraction      |
| \*       | multiplication   |
| /        | true division    |
| //       | integer division |
| %        | modulo operator  |

Usage:

- addition, subtraction, multiplication results depend on type supplied
  - if int an int is returned
  - if float float is returned
- division:
  - case of operands considered
  - \/ returns true division:
    - 27 \/ 4 ==> 6.75
  - \/\/ returns integer division:
    - 27 \/\/ 4 ==> 6
- semantics of \/\/ and \% with negative:
  - n: dividend
  - m: divisor
  - q = n \/\/ m
  - r = n \% m
  - python guarantees:
    - q \* m \+ r = n
    - 0 <= r < m
  - operators also extended to floating points
    - q = n \/\ m : is integer floor of the quotient
    - r = n \% m: is remainder such that q \* m \+ r = n

```python
 -27 // 4  #  (−7) ∗ 4 + 1 = −27"
 27  // -4 # 27 = (−7) ∗ (−4) + (−1)
```

#### Bitwise Operator

| Operator | Description                                 |
| -------- | ------------------------------------------- |
| ~        | bitwise complement (prefix unary operator)  |
| &        | bitwise and                                 |
| &#124;   | bitwise or                                  |
| ^        | bitwise exclusive or                        |
| <<       | shift bits left, filling in with zeros      |
| >>       | shift bits right, filling in with sign bits |

```python
1 << 2
5 >> 1
1 & 2
1 | 2
~3
4 ^ 2
```

#### **Sequence Operators**

- sequence types support syntax:
  - s[j]: index at j
  - **s[start:stop]**: slice including indices [start, stop)
  - **s[start:stop:step]**: slice including indices start + step,
    start \+ 2-step, ..., up to but not equal to stop
  - s \+ t concatenation of sequence
  - k \* s: shorthand for s \+ s \+ s \+ s ... (k times)
  - val in s: containment check
  - val not in s: not containment check

Details:

- val in s:
  - strings: single character in substring
- comparisons performed in lexographic order for all sequences
  - element by element comparison until first mismatch
    - s == t: equivalent (element by element)
    - s != t: not equivalent (element by element)
    - s < t: lexicographically less than
    - s <= t: lexicographically greater than
    - s > t: lexicographically greater than
    - s >= t: lexicographically greater than or equal to

#### sets and frozensets

| set operation | description                                  |
| ------------- | -------------------------------------------- |
| key in s      | is key member of set                         |
| key not in s  | is key not member of set                     |
| s1 == s2      | does s1 contain same elements as s2          |
| s1 != s2      | s1 does not contain identical elements to s2 |
| s1 <= s2      | s1 subset of s2                              |
| s1 < s2       | s1 proper subst of s2                        |
| s1 > s2       | s1 is proper superset of s2                  |
| s1 >= s2      | s1 is superset of s2                         |
| s1 &#124; s2  | union of s1 and s2                           |
| s1 & s2       | intersection of s2 and s2                    |
| s1 - s2       | set of elements in s1 but not in s2          |
| s1 ^ s2       | set of elements precisely in s1 or s2        |

NOTE: no guarantee in set order

#### dictionaries

- do not maintain order of elemens
- equivalence: dicta == dictb
- does sut support operators such as <
  - two dictionaries contain same key pairs
- supported operators:
  - d[key]: value associated with key
  - d[key] == value: set or reset value with given key
  - del d[key]: remove key associated with given dictionary
  - key in d: containment check
  - key not in d: non-containment check
  - d1 == d2: d1 is equivalent to d2
  - d1 != d2: d1 is not equivalent to d2

#### Extended Assignment Operators

- extended assignment operators (most supported)
  - count += 5
  - for immutable types such as number the identifier is assigned
    to a newly constructed value
  - lists += redefined to update list
- precedence:
  - operators with higher precedence will be evaluated before operators with lower precedence.
  - operators within a category are typically evaliated from left to right
  - unary and exponentiation are evaluated from right to left

| precendence | type                                           | example/operator                                                          |
| ----------- | ---------------------------------------------- | ------------------------------------------------------------------------- |
| 1           | member access                                  | expr.member                                                               |
| 2           | function/method calls and container subscripts | expr(...) and expr[...]                                                   |
| 3           | exponentiation                                 | **                                                                        |
| 4           | unary operators                                | +expr, -expr, ~expr                                                       |
| 5           | multiplication/division                        | *, /                                                                      |
| 6           | addition/subtraction                           | +, -                                                                      |
| 7           | bitwise shifting                               | <<, >>                                                                    |
| 8           | bitwise and                                    | &                                                                         |
| 9           | bitwise xor                                    | ^                                                                         |
| 10          | bitwise or                                     | &#124;                                                                    |
| 11          | comparison/containment                         | comparison: is, is not, ==, !=, <, <=, >, >, >=   containment: in, not in |
| 12          | logical-not                                    | not expr                                                                  |
| 13          | logical-and                                    | expr1 and expr2                                                           |
| 14          | logical-or                                     | expr1 or expr2                                                            |
| 15          | conditional                                    | val1 if cond else val2                                                    |
| 16          | assignment                                     | +, +=, -=, *=                                                             |

#### chained assignment

- multiple idenifiers to the rightmost value
- x = y = 0

#### chaining comparison

- expression 1 <= x + y <= 10 is evaluated as
  - (1 <= x + y) and (x + y <= 10)
- note: (x + y) is not evaluated twice

#### Control Flow

- colon character used to define block of code for body control structure
- body requires indentation

Conditionals

- if statement
  - each condition is a boolean statement
  - each body contains one or more commands that are executed sequentially
  - precisely one body will be executed
  - any number of elif clauses can instantiated (including zero)
  - else clause is optional
  - booleans for strings:
    - if response: will be True if response != ''
  - control structures may be nested

```python
if first_condition:
  first_body
  
elif second_condition:
  second_body

elif third_condition:
  third_body

else:
  fourth_body
```

#### While Loops

- condition can be arbitrary boolean expression
- if condition is True body is executed
- loop condition tested after loop body executes

```python
while condition:
  body
```

#### For Loops

- used for iterating through collections or series of items

```python
for element in iterable:
  body
```

#### Index-Based For Loops

- knowledge of index of an element within the sequence
- range: generates integer sequences
  - range(n): genenerates integers 0 to n-1

```python
total = 0
for j in range(len(data)):
  total += data[j]
```

#### Break Statements

immediately terminates a while or for loop when executed within the body

```python
found = False

for item in data:
  if item == target:
    found == True
    break
```

#### Continue Statements

- causes current iteration of loop body to stop

```python
  for i in range(20):
  # prints numbers 1 to 19 excluding 7

    if i == 7:
      continue
      print(i)
```

### Functions

- stateless function that is invoked without context
  - sorted(data)
- method: member function that is invoked upon a specific object
  - data.sort()
- body expressed in indented block of code
- activation record:
  - created each time function is called
  - stores relevant information for current call
  - namespace: manages all identifiers that have local scope within the current call
  - identifier in local scope have no relation to identifiers in callers scope
- return:
  - function should immediately cease execution
  - value returned to caller
  - None returned if statement is empty
  - multiple return statements allowed in function

```python

def count(data, target):  # serves as functions signature
  n = 0
  for item in data:
      if item == target:  # function body from after def to end
          n += 1
  return 1
```

#### Information Passing

- formal parameters: identifiers used to describe expected parameters
- actual parameters: objects sent by the caller when invoking the function
- standard assignment statement: when function is invoked, each identifier serves as formal parameter is assigned in the function's local scope.
- return value from function back to the caller is implemented as an assignment

#### Mutable Parameters

- mutable object parameters: state can be changed inside the called function

#### Default Parameter Values

- functions are polymorphic: more than one function signature
- default values for parameters allow for calling function with varying number of parameters
- def foo(a, b=15, c=27):
  - foo(20)
  - foo(20, 40)
  - foo(20, 40, 80)

#### Keyword Parameters

- positional arguments: traditional means of matching parameters to arguments
- keyword argument:
  - explicitly assigning actual parameters to a formal parameter
    - foo(c=5)
  - possible to require functions to specify certain arguments as keyword only
    - max(1, -3, key=abs)
    - max(1, 2, -54, -100)
    - key can not be specified positionally

#### built-in functions

| function                                                                                 | description                                                     |
| ---------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| abs(x)                                                                                   | absolute value of a number                                      |
| all(iterable)                                                                            | True if bool(e) is True for each element                        |
| any(iterable)                                                                            | True if bool(e) is True for at least one element                |
| chr(integer)                                                                             | one character string with the given unicode print               |
| divmod(x,y)                                                                              | return (x//y, x%y) as tuple , if x and y are int                |
| hash(obj)                                                                                | return integer hash value for object                            |
| id(obj)                                                                                  | reutrn unique integer serving as identity for object            |
| input(prompt) return string from standard input                                          |
| isiinstance(obj, cls)                                                                    | obj is instance of cls                                          |
| iter(iterable)                                                                           | new iterator for object for parameter                           |
| len(iterable)                                                                            | number of elements in a given iteration                         |
| map(f, iter1, iter2,...) return iterator yielding result of fucntion calls f(e1, e2, ..) |
| max(iterable)                                                                            | reutrn largest member                                           |
| min(iterable)                                                                            | smallest element                                                |
| next(iterator)                                                                           | return next element reported by iterator                        |
| open(filename, mode)                                                                     | open file with given name and access mode                       |
| ord(char)                                                                                | return unicode point of given character                         |
| pow(x,y)                                                                                 | reutrn x**y (as an integer if x and y are integers)             |
| pow(x,y,z)                                                                               | returrn x**y mod z as integer                                   |
| print(obj1, obj2,..) print arguments with separating spaces and trailing new line        |
| range(stop)                                                                              | iteration 0,1,...,stop-1                                        |
| range(start, stop)                                                                       | start, start+1, start+2,..stop-1                                |
| range(start, stop, step)                                                                 | start, start+step, start +2*step..                              |
| reversed(sequence)                                                                       | return iteration of sequence in reverse                         |
| round(x) return nearest int value (goes to closest even value in case of a tie)          |
| round(x,k) reutrn value rounded to nearest 10^-k                                         |
| sorted(iterable)                                                                         | reutrn list containing elements of the iterable in sorted order |
| sum(iterable)                                                                            | reutrn sum of elements in iterable (must be numeric)            |
| type(obj)                                                                                | reutnr class to which instance obj belongs                      |

### Simple Input and Output

#### console input and output

- print function:
  - standard output to the console
  - nonstring arguments will be displayed as str(x)
  - print('maroon', 5)
  - sep: used to change the separation
  - print('maroon', 5, sep=':')
  - end: character to print at end of print
    - default is '\n'
  - file: print to output file rather than console

#### input function

- used to get input from the user
- example:
  - year = int(input('In what year where you born? '))

#### Files

- open(): used to typically access files
  - 'w' or 'a' for writable files
  - 'r' for readable
- default filse are opened readonly

| method             | description                                                                                                                                                                |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| fp.read()          | return remaining contents of a file                                                                                                                                        |
| fp.read(k)         | return next k bytes of a readable file                                                                                                                                     |
| fp.readline()      | return remainder of current line as a sting                                                                                                                                |
| fp.redlines()      | return all remaining lines of the file as a list of strings                                                                                                                |
| for line in fp     | iterate through all remaining lines in readable file                                                                                                                       |
| fp.seak(k)         | change current position to the kth byte of the file                                                                                                                        |
| fp.tell()          | return curent position of the file                                                                                                                                         |
| fp.write(string)   | write given string at current position of the writable file                                                                                                                |
| fp.writelines(seq) | write each of th strins of the given sequence at the current position of the writable file. This command does not insert any newlines beyond what is embedd in the string. |
| print(..,file=fp)  | redirect output of print function to the file                                                                                                                              |

#### Exception Handling

- exceptions: objects that are raised (or thrown) by the code when encountering unexpected circumstances
- interpreter raises exceptions when it runs out of memery
- exceptions can be caught and handled by surrounding code
- uncaught exception causes the interpreter to stop executing the program and to report an appropriate error message

#### Common Exception Types

- Exception: base class for most error types
- AttributeError: raise by obj.foo. if obj has no member foo
- EOFError: if end of file reached for console or file output
- IOError: raised upon failure of I/O operation
- IndexError: raised if index to sequence is out of bonds
- KeyError: Raised if nonexistend key requested for set or dictionary
- KeyboardInterrupt: raied if user types ctrl-C while program is executing
- NameError: Raised if nonexistent identifier is used
- StopIteration: raised by next(iterator) if no element
- TypeError: raised when wrong type of parameter is sent to the function
- ValueError: raised when parameter has invalid value
- ZeroDivisionError: Raised when any division operator used with 0 as divisor

#### Raising an exception

- raise: used to throw an exception
  - raise ValueError('x cannot be negative')
- first validate it is appropriate type then appropriate value

```python
def sqrt(x):
  if not isinstance(x, (int, float)):  
    raise TypeError('x must be numeric')
  elif x < 0:
    raise ValueError('x cannot be negative')
```

#### Exception Handling Checking

- isinstance: used to check type
- abstract base class, collections.Iterable support for-loop syntax
- python checks values for addition inherently no need to add verbose error checking when built in provide clear message

```python
def sum(values):
    if not isinstance(values, collections.Iterable):
        raise TypeError( parameter must be an iterable type )
    total = 0
    for v in values:
        if not isinstance(v, (int, float)):
            raise TypeError( elements must be numeric )
        total = total+ v
    return total

def sum(values):
    total = 0
        for v in values:
    total = total + v
    return total
```

#### catching an exception

- python typically uses: it is easier to ask for forgiveness than it is to get permission
- try/except:
  - non-exceptional cases run efficiently
  - exceptional cases require special handling
  - useful if exceptions are rare and prohibitively expensive to proactively evaluate a condition to avoid the exception
  - can use tuple of erros to indicate types of errors to catch:
    - except (ValueError, EOFError)

```python
try:
    ratio = x / y
except ZeroDivisionError:
    ... do something else ...
```

```python
# do nothing with exception use "pass"

except (ValueError, EOFError):
    pass
```

#### Exception Guidance

- final "except:" clause without any identifiers will catch all unknown errors
  - used sparingly, dangerous to catch unknown errors
- finally clause: at the end of try catch will always be executed even with uncaught exceptions

### Modules and import statements

- **130-150 functions and classes** that are defined within Python's built-in namespace

- **modules**: how values and functions in standard Python distribution are organized

- **imported**: how modules can be used within a program

- **import**: loads defintions from a module into the current namespace

```python
# pi and sqrt are aded to current namespace
from math import pi, sqrt
```

- **importing many definitions**: used import \* sytax

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

#### Creating a New Module

Add defintions in file named with ".py" suffix

Example:

- place count fucntion into file named utility.py

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

#### Important Existing Modules

| Module Name | Description                                                   |
| ----------- | ------------------------------------------------------------- |
| array       | provides compact array storage for primitive types            |
| collections | additional data structures that involve collection of objects |
| copy        | functions for making copies of objects                        |
| heapq       | heap-based priority queue functions                           |
| math        | common mathematical functions                                 |
| os          | support for interaction with operating system                 |
| random      | random number generation                                      |
| re          | regular expression processing                                 |
| sys         | additional interaction methods with python interpreter        |
| time        | support for measuring time, or delaying a program             |

#### Pseudo-Random Number Generation

- **pseudo-random number generator** generates numbers that are statistically random
but not necessarily truly random

- deterministic formula that generate sthe next number in a sequence
- Mersenne twister: technique used by Python to generate random numbers
- next number in pseudo random number generator is deterministic

| Syntax                     | Description                                                                 |
| -------------------------- | --------------------------------------------------------------------------- |
| seed(hashable)             | initializes pseudo-random number generator based on hash value of parameter |
| random()                   | pseudo-random floating point between [0.0, 1.0)                             |
| randint(a,b)               | pseudo-random integer in closed interval [a, b]                             |
| randrange(start,stop,step) | random integer in standard python range specified by parameters             |
| choice(seq)                | returns element of a given sequence chosen randomly                         |
| shuffle(seq)               | reorders elements of a given sequence pseudo-randomly                       |

### Scopes and Namespacea

- **name resolution**: process of determining the value associated with the identifier

- **scope**: contains definitions made with identifiers

- **global scope**:  scope where top-level assignments take place

- **namespace**: abstraction used to represent eaach distinct scope
  - dictionaries are used to represent scopes

#### Functions to examine namespace

- **dir**: reports names and identifiers (keys in dictinary) in a given namespace
- **vars**: returns a full dictionary of items in local namespace

By default cals to **dir()** and **vars()** report the most locally enclosing namespace

- **searching for name**: when identifier is specified python searches series of namespaces for name resolution
  - first the most locally enclosing then next outer scope and so on

- **classes** can have there own namespace as well

#### First-Class objects

- **first-class objects** are instances of type tha can be assigned to an identifier, passed as a parameter, or returned by a function

- **functions are first class**: they satisfy the requirements

```python
# scream is an alias for print
scream = print
scream('Hello')
```

### Additional Python Conveniences

Useful python functionality for writing clear and consice code.

#### Conditional Expressions

##### **conditional expressions**: replace simple control structures

```python
expr1 if condition else expr2
```

Evaluate expr1 if condition is True otherwise expr2. Similar to ternary operator in C:

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

#### Comprehension Syntax

- **comprehension syntax**: produce one series based on evaluation of another series

##### **list comprehension**: generate a new list based on evaluating another sequence

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

##### **generator comprehension**: results do not have to be stored in memory

- can feed list comprehension directly to function

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