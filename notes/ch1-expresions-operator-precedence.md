### Expressions and Operator Precedence

 * expressions: combination of existing values using operators
 * compound expressions: require evaluation of two or more operators
 * precedence: determines order in which operators are evaluated

**Logical Operators**

|operator | description |
|---------|--------|
| not| unary negation |
| and| conditional and |
| or| conditional or |

Note: or and and operators short-circuit
  * if result can be determined based on value of first operand
  * useful for constructing boolean expressions 


**Equality Operators**

| operator | description |
|--------|--------|
| is | same identity  evaluates to True if a and b are aliases to same object |
| is not | different identity  evaluates to Trueif not aliases to same object |
| == | equivalent evaluates to true if a nd be refer to the same or different objects that evaluate to same value |
| != | not equivalent |

**Comparison Operators**

| Operator | Description |
|--------|--------|
| < | less than |
| <= | less than or equal to |
| > | greater than |
| >= | greater than or equal to |
 
Works for datatypes that have natural order:
  * defined lexicograhically and case sensitively for strings
  * exception raise if operands incompatible types

```python
2 > 4
"bye" < "hello"
```
**Arithmetic Operators**

| Operator | Description |
|--------|--------|
| \+ | addition |
| \- | subtraction |
| \* | multiplication |
| / | true division |
| // | integer division |
| % | modulo operator |

Usage:
  * addition, subtraction, multiplication results depend on type supplied:
    * if int an int is returned
    * if float float is returned
  * division:
      * case of operands considered
      * \/ returns true division:
        * 27 \/ 4 ==> 6.75
      * \/\/ returns integer division:
        * 27 \/\/ 4 ==> 6
  * semantics of \/\/ and \% with negative:
    * n: dividend
    * m: divisor
    * q = n \/\/ m
    * r = n \% m
    * python guarantees: 
      * q \* m \+ r = n
      * 0 <= r < m
    * operators also extended to floating points
      * q = n \/\ m : is integer floor of the quotient
      * r = n \% m: is remainder such that q \* m \+ r = n

```python
 -27 // 4  #  (−7) ∗ 4 + 1 = −27"
 27  // -4 # 27 = (−7) ∗ (−4) + (−1)
```

**Bitwise Operator**
March 8, 2019 8:06 PM| column | column |

| Operator | Description |
|--------|--------|
| ~  | bitwise complement (prefix unary operator) |
| &  | bitwise and |
| &#124; | bitwise or |
| ^  | bitwise exclusive or |
| << | shift bits left, filling in with zeros |
| >> | shift bits right, filling in with sign bits |


```python
1 << 2
5 >> 1
1 & 2
1 | 2
~3
4 ^ 2
```

**Sequence Operators**
   * sequence types support syntax:
     * s[j]: index at j
     * **s[start:stop]**: slice including indices [start, stop)
     * **s[start:stop:step]**: slice including indices start + step,
       start \+ 2*step, ..., up to but not equal to stop
     * s \+ t concatenation of sequence
     * k \* s: shorthand for s \+ s \+ s \+ s ... (k times)
     * val in s: containment check
     * val not in s: not containment check

Details:
  * val in s: 
    * strings: single character in substring
  * comparisons performed in lexographic order for all sequences
    * element by element comparison until first mismatch
      * s == t: equivalent (element by element)
      * s != t: not equivalent (element by element)
      * s < t: lexicographically less than
      * s <= t: lexicographically greater than
      * s > t: lexicographically greater than
      * s >= t: lexicographically greater than or equal to


**sets and frozensets**

| set operation | description |
|--------|--------|
| key in s | is key member of set |
| key not in s | is key not member of set |
| s1 == s2  | does s1 contain same elements as s2 |
| s1 != s2 | s1 does not contain identical elements to s2 |
| s1 <= s2 | s1 subset of s2 |
| s1 < s2 | s1 proper subst of s2 |
| s1 > s2 | s1 is proper superset of s2 |
| s1 >= s2 | s1 is superset of s2 |
| s1 &#124; s2 | union of s1 and s2 |
| s1 & s2 | intersection of s2 and s2 |
| s1 - s2 | set of elements in s1 but not in s2 |
| s1 ^ s2 | set of elements precisely in s1 or s2 |

NOTE: no guarantee in set order


**dictionaries**
  * do not maintain order of elemens
  * equivalence: dicta == dictb
  * does sut support operators such as <
    * two dictionaries contain same key pairs
  * supported operators:
    * d[key]: value associated with key
    * d[key] == value: set or reset value with given key
    * del d[key]: remove key associated with given dictionary
    * key in d: containment check
    * key not in d: non-containment check
    * d1 == d2: d1 is equivalent to d2
    * d1 != d2: d1 is not equivalent to d2

**Extended Assignment Operators**
  * extended assignment operators (most supported)
    * count += 5
    * for immutable types such as number the identifier is assigned 
      to a newly constructed value
    * lists += redefined to update list
  * precedence:
    * operators with higher precedence will be evaluated before operators with lower precedence.
    * operators within a category are typically evaliated from left to right
    * unary and exponentiation are evaluated from right to left

| precendence | type | example/operator |
|--------|--------|--------|
|   1    | member access | expr.member |
|   2    | function/method calls and container subscripts | expr(...) and expr[...] |
|   3    | exponentiation | ** |
|   4    | unary operators | +expr, -expr, ~expr |
|   5    | multiplication/division | *, / |
|   6    | addition/subtraction | +, - |
|   7    | bitwise shifting | <<, >> |
|   8    | bitwise and | & |
|   9    | bitwise xor | ^ |
|   10    | bitwise or | &#124;  |
|   11    | comparison/containment |  comparison: is, is not, ==, !=, <, <=, >, >, >=   containment: in, not in| 
|   12    | logical-not | not expr  |
|   13    | logical-and | expr1 and expr2 |
|   14    | logical-or | expr1 or expr2 |
|   15    | conditional | val1 if cond else val2 |
|   16    | assignment | +, +=, -=, *= |

**chained assignment**
  * multiple idenifiers to the rightmost value
  * x = y = 0

**chaining comparison**
  * expression 1 <= x + y <= 10 is evaluated as
    * (1 <= x + y) and (x + y <= 10)
  * note: (x + y) is not evaluated twice

**Control Flow**
  * colon character used to define block of code for body control structure
  * body requires indentation

**Conditionals**
  * if statement
    * each condition is a boolean statement
    * each body contains one or more commands that are executed sequentially
    * precisely one body will be executed
    * any number of elif clauses can instantiated (including zero)
    * else clause is optional
    * booleans for strings:
      * if response: will be True if response != ''
    * control structures may be nested

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

**While Loops**
  * condition can be arbitrary boolean expression
  * if condition is True body is executed
  * loop condition tested after loop body executes

```python
while condition:
  body
```

**For Loops**
  * used for iterating through collections or series of items

```python
for element in iterable:
  body
```

**Index-Based For Loops**
  * knowledge of index of an element within the sequence
  * range: generates integer sequences
    * range(n): genenerates integers 0 to n-1

```python
total = 0
for j in range(len(data)):
  total += data[j]
```

**Break Statements**
  * immediately terminates a while or for loop when executed within 
    the body

```python
found = False

for item in data:
  if item == target:
    found == True
    break
```

**Continue Statements**
  * causes current iteration of loop body to stop
```python
for i in range(20):
	# prints numbers 1 to 19 excluding 7	
	if i == 7:
    	continue
    print(i)
```

### Functions
  * stateless function that is invoked without context
    * sorted(data)
  * method: member function that is invoked upon a specific object
    * data.sort()
  * body expressed in indented block of code
  * activation record:
    * created each time function is called 
    * stores relevant information for current call
    * namespace: manages all identifiers that have local scope within the current call
    * identifier in local scope have no relation to identifiers in callers scope
  * return: 
    * function should immediately cease execution 
    * value returned to caller
    * None returned if statement is empty 
    * multiple return statements allowed in function

```python

def count(data, target):  # serves as functions signature
  n = 0
  for item in data:
      if item == target:  # function body from after def to end
          n += 1
  return 1
```

#### Information Passing
  * formal parameters: identifiers used to describe expected parameters
  * actual parameters: objects sent by the caller when invoking the function
  * standard assignment statement: when function is invoked, each identifier serves as formal parameter is assigned in the function's local scope. 
  * return value from function back to the caller is implemented as an assignment


#### Mutable Parameters
  * mutable object parameters: state can be changed inside the 
        called function

#### Default Parameter Values
  * functions are polymorphic: more than one function signature
  * default values for parameters allow for calling function with
    varying number of parameters
  * def foo(a, b=15, c=27):
    * foo(20)
    * foo(20, 40)
    * foo(20, 40, 80)

#### Keyword Parameters
  * positional arguments: traditional means of matching parameters to arguments
  * keyword argument:
    * explicitly assigning actual parameters to a formal parameter
      * foo(c=5)
    * possible to require functions to specify certain arguments as keyword only
      * max(1, -3, key=abs)
      * max(1, 2, -54, -100)
      * key can not be specified positionally

#### built-in functions

| function | description|
|--------|--------|
| abs(x) |  absolute value of a number |
| all(iterable) |  True if bool(e) is True for each element |
| any(iterable) |  True if bool(e) is True for at least one element |
| chr(integer) |  one character string with the given unicode print |
| divmod(x,y) |  return (x//y, x%y) as tuple , if x and y are int |
| hash(obj) |  return integer hash value for object |
| id(obj) |  reutrn unique integer serving as identity for object |
| input(prompt) return string from standard input |
| isiinstance(obj, cls) |  obj is instance of cls |
| iter(iterable) |  new iterator for object for parameter |
| len(iterable) |  number of elements in a given iteration |
| map(f, iter1, iter2,...) return iterator yielding result of fucntion calls f(e1, e2, ..)  |
| max(iterable) |  reutrn largest member |
| min(iterable) |  smallest element |
| next(iterator) |  return next element reported by iterator |
| open(filename, mode) |  open file with given name and access mode |
| ord(char) |  return unicode point of given character |
| pow(x,y) |  reutrn x**y (as an integer if x and y are integers) |
| pow(x,y,z) |  returrn x**y mod z as integer |
| print(obj1, obj2,..) print arguments with separating spaces and trailing new line |
| range(stop) |  iteration 0,1,...,stop-1 |
| range(start, stop) |  start, start+1, start+2,..stop-1 |
| range(start, stop, step) |  start, start+step, start +2*step.. |
| reversed(sequence) |  return iteration of sequence in reverse |
| round(x) return nearest int value (goes to closest even value in case of a tie) |
| round(x,k) reutrn value rounded to nearest 10^-k |
| sorted(iterable) |  reutrn list containing elements of the iterable in sorted order |
| sum(iterable) |  reutrn sum of elements in iterable (must be numeric) |
| type(obj) |  reutnr class to which instance obj belongs |

### Simple Input and Output

#### console input and output
  * print function: 
    * standard output to the console
    * nonstring arguments will be displayed as str(x)
    * print('maroon', 5)
    * sep: used to change the separation
    * print('maroon', 5, sep=':')
    * end: character to print at end of print
    	* default is '\n'
    * file: print to output file rather than console

#### input function
  * used to get input from the user
  * example:
     * year = int(input('In what year where you born? '))

#### Files
  * open(): used to typically access files
    * 'w' or 'a' for writable files
    * 'r' for readable
  * default filse are opened readonly

| method | description |
|-----------|-------------|    
| fp.read() |  return remaining contents of a file |
| fp.read(k) |  return next k bytes of a readable file |
| fp.readline() |  return remainder of current line as a sting |
| fp.redlines() |  return all remaining lines of the file as a list of strings |
| for line in fp |  iterate through all remaining lines in readable file |
| fp.seak(k) |  change current position to the kth byte of the file |
| fp.tell() |  return curent position of the file |
| fp.write(string) |  write given string at current position of the writable file |
| fp.writelines(seq) |  write each of th strins of the given sequence at the current position of the writable file. This command does not insert any newlines beyond what is embedd in the string. |
| print(..,file=fp) |  redirect output of print function to the file |

#### Exception Handling
  * exceptions: objects that are raised (or thrown) by the code when encountering unexpected circumstances
  * interpreter raises exceptions when it runs out of memery
  * exceptions can be caught and handled by surrounding code
  * uncaught exception causes the interpreter to stop executing the program and to report an appropriate error message

#### Common Exception Types
  * Exception: base class for most error types
  * AttributeError: raise by obj.foo. if obj has no member foo
  * EOFError: if end of file reached for console or file output
  * IOError: raised upon failure of I/O operation
  * IndexError: raised if index to sequence is out of bonds
  * KeyError: Raised if nonexistend key requested for set or dictionary
  * KeyboardInterrupt: raied if user types ctrl-C while program is executing
  * NameError: Raised if nonexistent identifier is used
  * StopIteration: raised by next(iterator) if no element
  * TypeError: raised when wrong type of parameter is sent to the function
  * ValueError: raised when parameter has invalid value
  * ZeroDivisionError: Raised when any division operator used with 0 as divisor

#### Raising an exception
  * raise: used to throw an exception
    * raise ValueError('x cannot be negative')
  * first validate it is appropriate type then appropriate value

```python
def sqrt(x):
  if not isinstance(x, (int, float)):  
    raise TypeError('x must be numeric')
  elif x < 0:
    raise ValueError('x cannot be negative')
```

#### Exception Handling
  * isinstance: used to check type
  * abstract base class, collections.Iterable support for-loop syntax
  * python checks values for addition inherently no need to add verbose error checking when built in provide clear message


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

### catching an exception
  * python typically uses: it is easier to ask for forgiveness than it is to get permission
  * try/except:
    * non-exceptional cases run efficiently
    * exceptional cases require special handling
    * useful if exceptions are rare and prohibitively expensive to proactively evaluate a condition to avoid the exception
    * can use tuple of erros to indicate types of errors to catch:
      * except (ValueError, EOFError)


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

#### Exception guidance
  * final "except:" clause without any identifiers will catch all 
    unknown errors
    * used sparingly, dangerous to catch unknown errors
  * finally clause: at the end of try catch will always be executed 
    even with uncaught exceptions
