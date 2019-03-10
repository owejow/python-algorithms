# Python Review

## chapter 1: Python Primer

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