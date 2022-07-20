---
author: "Dhruv Sharma"
date: 2022-07-18
title: Map, Filter, Reduce in python
type:
- post
- posts
weight: 10
tags:
  - python
  - tech
---


```python
     li = [x for x in range(100)]
```

## map:
```python
  li = list(map(lambda x : x/2,li))
```

- map(function,iteritable)
- return a map object after applying given function to all elements of, which can be
  then converted to a list
  iteritable
- equivalent to

```python
  for x in li:
      x = x/2
```

## filter:

```python
  even = list(filter(lambda x : x%2 == 0 ,li))
```

- filter(function,iteritable)
- return a filter object after applying given function to all elements
  of iteritable
- equivalent to

```python
  even = []
  for x in li:
      if x%2 == 0 :
          even.append(x)
```

## reduce:

```python
  from functools import reduce
  maxx = reduce( lambda x,y : x if x > y else y, li)
  print(maxx)
```

- reduce(function,iteritable)
- have to import it from functools module
- return a map object after applying given function to all elements of
  iteritable
- equivalent to

```python
  y = li[0]
  maxx = y
  for x in li:
      if x > y :
          maxx = x
      else :
          maxx = y
  print(maxx)
```
