# Scopes and Namespacea

**name resolution**: process of determining the value associated with the identifier

**scope**: contains definitions made with identifiers

**global scope**:  scope where top-level assignments take place

**namespace**: abstraction used to represent eaach distinct scope
  * dictionaries are used to represent scopes

### Functions to examine namespace

**dir**: reports names and identifiers (keys in dictinary) in a given namespace
**vars**: returns a full dictionary of items in local namespace

By default cals to **dir()** and **vars()** report the most locally enclosing namespace

**searching for name**: when identifier is specified python searches series of namespaces
for name resolution
  * first the most locally enclosing then next outer scope and so on

**classes** can have there own namespace as well


### First-Class objects

**first-class objects** are instances of type tha can be assigned to an identifier, 
passed as a parameter, or returned by a function

**functions are first class**: they satisfy the requirements

```python
# scream is an alias for print
scream = print
scream('Hello')
```