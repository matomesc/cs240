# Intro
## Objectives

- efficiently process large bodies of data
- storing, accessing and maintaining (insert/removes, sort)

## Emphasis

- design and analysis of efficient data structs and algos
- mathematical proofs
- implementation

## Preliminaries

- abstract data type (ADT)
  - it's characterized by the supported operations
  - eg. ADT dictionary implements `insert(k, v)`, `remove(k)`, `get(k)`

## Data Structure

- concrete implementation of ADTs + operators
- eg. linked lists, arrays, binary search trees

## Topics

- analysis of algorithms
- ADT priority queues
- sorting
- ADT dictinary
- string and text processing
- compression

## Unit Cost Model

We'll use the RAM model to analyze cost:

- fetch / storing word of memory
- arithmetic operations

all run in constant time

[ Log cost model: better arithmetic on large #s takes more time ~  # of digits in n ~ log n ]

RAM is finite and bounded. Sometimes it fits in RAM but what happens when it doesn't?

- use disk
  - much much slower
  - need to optimize disk IO

### Memory hierarchy

1. registers (less data / fast)
2. CPU Cache
3. RAM
4. disk
5. network (more data / slow)

## Math

- floor(n)
- ceil(n)
- arithmetic sum
- geometric sum
- harmonic sum ( H = 1 + 1/2 + 1/3 + 1/4 + ... + 1/n ~ log n + c)
- fibonacci
  - F(n) = F(n - 1) + F(n - 2)

```
let x = lim (F(n)/F(n-1), n->INF)
      = lim (1 + F(n - 2)/F(n-1), n->INF)
      = 1 + 1/x
      => x = phi
```

### Stirling's Approximation

More [here](http://en.wikipedia.org/wiki/Stirling's_approximation)

## Analysis of Algorithms

- let n = size of data
- best case anaysis: minimum cost as a fn of n
- worst case: maximum cost
- average case analysis: average cost / all inputs of size n
  - generally we need to know a bit about our data set to use avg case analysis (ie. is it mostly sorted)
- amortized analysis
  - in a sequence of several cheap operations, pay for a few expensive operations

What cost are we measuring?

- time (# of operations)
- space (RAM)