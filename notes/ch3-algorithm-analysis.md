# Python Study

- [Python Study](#python-study)
  - [Algorithm Analysis](#algorithm-analysis)
    - [Experimental Studies](#experimental-studies)
      - [Challenges of Experimental Analysis](#challenges-of-experimental-analysis)
      - [Beyond experimental analysis](#beyond-experimental-analysis)
        - [**Counting Primitive Operations**](#counting-primitive-operations)
    - [Seven Important Functions in Algorithm Analysis](#seven-important-functions-in-algorithm-analysis)
      - [The Constant Function](#the-constant-function)
      - [The Logarithmic Function](#the-logarithmic-function)
        - [Logarithm Rules](#logarithm-rules)
      - [The Linear Function](#the-linear-function)
      - [The N-Log-N Function](#the-n-log-n-function)
      - [The Quadratic Function](#the-quadratic-function)
      - [Cubic function and other polynomials](#cubic-function-and-other-polynomials)
        - [Summations](#summations)
      - [The Exponential Function](#the-exponential-function)
        - [Exponent Rules](#exponent-rules)
        - [Geometric Sums](#geometric-sums)
      - [Comparing grown rates](#comparing-grown-rates)
        - [Ceiling and Floor Functions](#ceiling-and-floor-functions)
    - [Asymptotic Analysis](#asymptotic-analysis)
      - [The "Big-Oh" Notation](#the-%22big-oh%22-notation)
      - [Properties of Big-Oh Notation](#properties-of-big-oh-notation)
      - [Big-Omega](#big-omega)
      - [Big-Theta](#big-theta)
      - [Comparative Analysis](#comparative-analysis)
      - [Examples of Algorithm Analysis](#examples-of-algorithm-analysis)
        - [$O(1)$ constant time operations](#o1-constant-time-operations)
        - [$O(n)$ Linear time](#on-linear-time)
        - [Prefix Averages](#prefix-averages)
          - [Quadratic Time Algorithm](#quadratic-time-algorithm)
          - [Linear-Time Algorithm](#linear-time-algorithm)
          - [Three-Way Set Disjointness](#three-way-set-disjointness)
    - [Useful formulas](#useful-formulas)

## Algorithm Analysis

### Experimental Studies

- **data structure** is a systematic way of organizing and accessing data
- **algorithm** a step-by-step procedure for performing some task in a finite amount of time.

#### Challenges of Experimental Analysis

- runtime of two algorithms difficult to compare unless experiments are performed in the same hardware and software environments
- only a limited set of test inputs can be run experimentally
- algorithm must be fully implemented to run it and experiment on it

#### Beyond experimental analysis

Goal is to

1. allow analysis of algorithms in a way that is independent of the hardware and software environment
2. study high-level description of algorithm without need for implementation
3. takes all possible inputs into consideration

##### **Counting Primitive Operations**

**primitive operation** corresponds to a low-level instruction with an execution time that is constant. Example primitive operations:

- assigning an identifier to an object
- determining the object associated with an identifier
- performing an arithmetic operation
- comparing two numbers
- asscessing a single element of a python list by index
- calling a function (excludes operations executed in the function)
- returning from a function

Count of primitive operations are used to measure the running time of an algorithm

**order of growth** for each function $f(n)$ that characterizes the number of primitive operations that are performed as a function of input size $n$

**average case** analysis difficult because typically we don't have probability distribution on the set of inputs

**worst case** can be analyzed so long as the worst-case input can be identified. If algorithm performs well on worst-case it will do well on all possible valid inputs.

### Seven Important Functions in Algorithm Analysis

#### The Constant Function

**constant function** for any input value $n$ the function assigns a constant value.

- $f(n) = c$

#### The Logarithmic Function

**logarithmic function**  most common base for logarithmic function is 2

- $x = log_{b} n$ if and only if $b^x = n$:w
- default base is 2: $log(n) = log_{2}(n)$

##### Logarithm Rules

1. $log_{b}(ac) = log_b{a} + log_b{c}$
1. $log_{b}(\frac{a}{c}) = log_{b}a - log_{b} c$
1. $log_{b}(a^c) = \frac{log_{d}a}{log_{d}b}$
1. $log_{b}(a) = \frac{log_{d}a}{log_{d}b}$
1. $b^{log_{d}a} = a^{log_{d}b}$

By convention $log\ n^c$ is the same as  $log(n^c)$

Can compute log base 2 in calculator:

- $log_2 n - \frac{log(n)}{log(2)}$

#### The Linear Function

**linear function** shows up in algorithmic analysis when a single basic operation is performed for each of the n elements in the input

- $f(n) = n$

#### The N-Log-N Function

**n-log-n** function grows little more rapidly than linear function and a lot less rapidly than the quadratic function

- $f(n) = n\ log(n)$

#### The Quadratic Function

**quadratic function** the main location where this appears in algorithms is in nested loops.

- $f(n) = n^2$

**quadratic function** if number of operations inside nested loops when the first operation takes one step, second two steps and so on.

- $1 + 2 + 3 + ... + (n-1) + n = \frac{n(n+1)}{2}$

#### Cubic function and other polynomials

**cubic function**: $f(n) = n^3$

**polynomial** function has input of the following form:

- $f(n) = a_0 + a_1n + a_2n^2 + ... a_dn^d$
  - $a_0, a_1, ... a_d$ are constants or coefficients of polynomial and $a_d \ne 0$
  - constant, linear and quadratic algorithms are subclases of the polynomial.

##### Summations

**summation** very occurring in the context of algorithms

- $\sum_{i=a}^{b} = f(a) + f(a+1) + f(a+2) + ... + f(b)$
- $\sum_{i=1}^{n} i = \frac{n(n+1)}{2}$
- polynomial of degree n:
  - $f(n) = \sum_{i=0}^{d} a_in^i$

#### The Exponential Function

**exponential function** the base $b$ is a positive constant and the argument $n$ is the exponent.

- $f(n) = b^n$
- base of 2 is the most common
- integer containing $n$ bits can represent all nonnegative integers less than 2^n
- a loop that starts by performing one operation and then doubles the number of operations performed with each iteration would have performed $2^n$ operations by the nth loop

##### Exponent Rules

Given positive integers a, b, and c:

- $(b^a)^c = b^{ac}$
- $b^ab^c = b^{a+c}$
- $\frac{b^a}{b^c} = b^{a-c}$

Exponential functions can be extended to real numbers or fractions.

- $b^{\frac{1}{k}}$ is defined to be $k^{th}$ root of $b$
- $b^{\frac{a}{c}} = (b^a)^\frac{1}{c}$

##### Geometric Sums

For any integer $n \ge 0$ and any real number a such that $a \gt 0$ and $a \ne 1$, the summation:

$\sum_{i=0}^n a^i = 1 + a + a^2 + ... a^3$

(remembering $a^0 = 1 if a \gt 0$) This summation equals:

$\frac{a^{n+1} - 1}{a-1}$

#### Comparing grown rates

| constant | logarithm | linear | n-log-n     | quadratic | cubic | exponential |
| -------- | --------- | ------ | ----------- | --------- | ----- | ----------- |
| $1$      | $log(n)$  | $n$    | $n\ log(n)$ | $n^2$     | $n^3$ | $a^n$       |

Exponential function grows the fastest as n grows larger

##### Ceiling and Floor Functions

**floor function**:

- $\lfloor{x}\rfloor =$ the largest integer less than or equal to $x$
- $\lceil{x}\rceil =$ the smallest integer greater than or equal to $x$

### Asymptotic Analysis

enough to understand how runtime **grows proportionally** to input

#### The "Big-Oh" Notation

Let $f(n)$ and $g(n)$ be functions mapping positive integers to positive real numbers. We say that $f(n)$ is $O(g(n))$ if there is a real constant $c > 0$ and an integer constant $n_0 \ge 1$ such that

$f(n) \le cg(n)$, for $n \ge n_0$

Allows us to say that a $f(n)$ is less than or equal to another function $g(n)$ up to a constant factor and in the **asymptotic** sense as $n$ grows toward infinity

- it is not considered good to say $f(n) \le O(g(n))$ it is better to say
  - $f(n) is O(g(n))$
  - $f(n) is order of O(g(n))$
  - $f(n) \in O(g(n))$
    - $\in$ is called in

#### Properties of Big-Oh Notation

Highest degree term in a polynomial is the term that determines the asymptotic growth rate of a polynomial. If f(n) is a polynomial of degree d, that is:

$f(n) - a_0 + a_1n + ... a_dn^d$

and $a_d > 0$, then $f(n)$ is $O(n^d)$

Characterize a function in the **simplest terms**.

#### Big-Omega

Let $f(n)$ and $g(n)$ be functions mapping positive integers to positive real numbers. We say that $f(n)$ is $\Omega(g(n))$ if $g(n)$ is $O(f(n))$. That is there is a real constant $c > 0$ and integer contant $n_0 \ge 1$ such that

$f(n) \ge cg(n)$ for $n \ge n_0$

#### Big-Theta

Big $\Theta$ says that two functions grow at the same rate up to constant factors. A function $f(n)$ is $\Theta(g(n))$ if $f(n)$ is $O(g(n))$ and $f(n)$ is $\Omega(g(n))$

- $c^\prime g(n) \le f(n) \le c^{\prime\prime} g(n)$ for $n \ge n_0$
- Example $3\ n\ log(n)  + 4n + 5\ log(n)$ is $\Theta(n\ log(n))$

#### Comparative Analysis

A program can be asymptotically better than another algorithm even though it can be faster for small value of n

Maximum problem that can be solved


Running Time $\mu$s| 1 second | 1 minute | 1 hour
---------|----------|---------|----------|-------
 $400n$ | 2500 | 150,000 | 9,000,000
 $2n^2$ | 707 | 5,477 | 42,426
 $2^n$ | 19 | 25 | 31

 Big-O Caution

- Asymptotic notations can hide very large constant factors
- $O(n^c)$A for constant $c \ge 1$ and those for $O(b^n)$ for some constant $b \ge 1$

#### Examples of Algorithm Analysis

##### $O(1)$ constant time operations

- len(data) is evaluated in constant time because the list class maintains an instance variable that records the current length of the list
- list access for integer index is implemented as an **array-based sequences**. References to a list's elements are stored in a consecutive block of memory.$j^{th}$ element of a list can be found by validating the index and using it as an offset into the underlying array

##### $O(n)$ Linear time

- maximum of a sequence. The loop executes n times and it performs one comparison and possibly one assignment statement

##### Prefix Averages

- **prefix average** given a sequence $S$ of n numbers compute the sequence $A$ such that $A[j]$ is the average of the elements $S[0],...,S[j]$, for $j=0,...,n-1$
  - $A[j] = \frac{\Sigma_{i=0}^jS[i]}{j+1}$

###### Quadratic Time Algorithm

```python

# total runtime O(n^2)
def prefix_average1(S):
    n = len(S)    # constant time
    A = [0] *n    # O(n) constant primitive ops

    # two nested for loops
    for j in range(n):
        total = 0   # executed n times
        for i in range(j+1):  # executed n times
            total += S[i] # executed 1 + 2 +... + n times
        A[j] = total / (j + 1)  # executed n times
    return A
```

###### Linear-Time Algorithm

```python
def prefix_average3(S):
    n = len(S)  # constant time
    A = [0] * n # takes O(n) constant primitive ops
    total = 0

    for j in range(n): # takes O(n)
        total += S[j]   # Constant time
        A[j] = total / (j+1) #  constant time
```

###### Three-Way Set Disjointness

**three-way set disjointness** problem is to determine if the intersection of the three sequences is empty:

- determing if there is an $x$ such that $x \in A, x \in B, x \in C$

####### Disjontness $O(n^3)$

```python
def disjoint1(A, B, C):
    for a in A:
        for b in B:
            for c in C:
                if a == b == c:
                    return False
    return True
```

####### Disjontness $O(n^2)$

```python
def disjoint1(A, B, C):
    for a in A:
        for b in B:
            if (a == b):  # only n sets of distinct elements to consider, the inner loop executes at most O(n) times
                for c in C:
                    if a == c:
                        return False
    return True
```


####### Disjontness $O(n^2)

### Useful formulas

- Harmonic number is $O(log\ n)$
  - $H_n = \Sigma_{j=1}^n \frac{1}{j}$ 