### Identifiers:
**identifiers** are:
  * case sensitive
  * aka name
  * assignment statement sets values

### Reserved words
 * can not be identifier
  * list of reserved words:
  
```python
False None True and as assert break class continue def

del elif else from in except global is finally  if

lambda for import nonlocal not or pass raise return try

while with yield
```

**Dynamically typed**
  * no type specified
  * alias second identifier assigned to object

**instantiation**
  * creating a new class 
  * invoke constructor:
      * Widget()
  * literal constructor:
      * temperature = 98.6
      * temperature = float(98.6)

```python
float(98.6) == 98.6
```

**methods**
  * member function that are part of specific instance of a class
  * [4, 1, 3].sort()

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

**method types**
  * mutators or update methods: change the state of object
  * accessors return information about state of object 
    but do not change its state

### Built-in class Types

| class | description |
|--------|--------|
| bool| boolean value (immutable) |
| int| integer value (immutable) |
| float| float value (immutable) |
| list| sequence of objects (mutable) |
| tuple| sequence of object (immutable) |
| str| character string (immutable) |
| set| unordered set of distinct objects (mutable) |
| frozenset| set of distinct objects (immutable) |
| dict |  dictionary (mutable) |

**bool**
  * values:
    * True 
    * False
  * bool: constructor, returns False by default
  * values to constructor determine bool return value
     * interpretation of value depends on type
         * numbers 0 return False all else True
         * lists and sequences, non-empty True, empty False

```python
bool()

bool(1)

bool(0)

bool([])

bool([0])
```

**int**
  * represents integer values of arbitrary magnitude
  * python automatically chooses the internal representation that is most suitable
    * does not have short or long like C++ or Java
  * Literals
    * integer values with sign: 0, -23, 43
    * Use octal, binary, or hexadecimal
       * 0 plus b binary: 0b111
       * 0 plus o octal: 0o44
       * 0 plus x hexadecimal: 0xff
    * constructor
       * int
       * returns 0 by default
       * truncates floats to integer
          * int(3.12) => 3
       * integer strings are converted to integer
          * int('33') => 33
          * default assumes base 10
          * if base is not decimal need to specify base
            * int('33',5) => 33
          * raises TypeError if value is not convertible
            * int('hello')****int
```python
int(3.12)
int("33", 5)
```

**float**
* sole floating point
  * uses fixed precision representation similar to double in Java and C++
  * literals
    * Trailing zeros are optional:
        * 4.0 can be represented as 4.
    * scientific notation
        * 6.023e23
  * constructor
    * float
    * returns 0.0 by default
    * attempts to convert string as floating point value
    * raises ValueError if not convertible

```python
float(3.12)
float("33")
```

### sequence types
  * list
  * tuple
  * string

**list**
  * stores sequence of objects
  * referential structure: stores reference to sequence of objects
  * array-based sequences that are zero-indexed
  * dynamically expland and contract
  * constructor:
    * list()
    * produces empty list by default
    * accepts any parameter that is iterable
    * list('hello') => ['h','e','l','l','o']

```python
list() # ()
[1,2]
```

**tuple**
  * immutable version of a sequence
  * can be more efficiently represented
  * delimeted by parenthesis
  * single element tuple: (17,)
    * (17) viewed as simple parenthesized numeric expression
  * constructor:
    * tuple
    * default: returns empty tuple

```python
tuple() # ()
(1,) # (1, )
(1,2)
```

**string**
   * str class stores immutable sequence of characters
   * literal:
      * single quotes: 'hello'
      * double quotes: "hello"
      * escaped quote delimiter:
        * 'Don\'t worry'
      * escaped characters
        * newline: \n
        * unicode: \u: \u20AC
      * using """ and ''' to delimit multiline
        * can embed newline naturally 

```python
"""Welcome to the GPA
   calculator
"""
```

**set**
  * collection of elements without duplicates
  * highly optimized for checking if element is in a set
  * restrictions
    * elements not placed in particular order
    * uses hash table as data structure
    * only immutable types can be place in set
      * supports tuples but not lists
    * set of frozensets can belong to a set 
  * constructor: 
    * literal: curly braces used as delimiter for the set
      * {17} or {'red', 'green', 'blue'}
    * set() used to create empty set
      * dictionary is returned with empty curly braces
    * iterable parameters presented in constructor return 
      set of distinct elements
      * set('hello') => {'h', 'e', 'o', 'l'}
```python
set() # returns set()
set('hello')  # returns {'l', 'e', 'o', 'h'} 
```

**frozenset**
  * immutable collection of elements without duplicates
  * constructor:
    * frozenset() -> empty frozenset object
    * frozenset(iterable) -> frozenset object
```python
frozenset() # returns frozenset()
frozenset('hello') # returns frozenset({'l', 'e', 'o', 'h'})
```

**dict class**
  * dictionary or mapping for set of distinct keys to values
  * almost identical to set except associated value is stored
  * literal:
    * curly braces to initialize
    * {} initializes empty dictionary
    * {'ga': 'Irish', 'de': 'German'}
  * constructor:
    * dict:
        * accepts mappings as a parameter and creates a new dictionary
          with identical association
        * key value pairs as parameters
          * dict{[('ga', 'Irish'), ('de', 'German')]}

```python
dict()  #  returns {}
dict([('ga', 'Irish'), ('de', 'German')]) # returns {'ga': 'Irish', 'de': 'German'}
{'ir': 'Iran', 'en': 'USA'}  # returns {'ir': 'Iran', 'en': 'USA'} 
```