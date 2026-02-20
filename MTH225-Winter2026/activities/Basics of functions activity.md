# MTH 225: Basic ideas of functions activity

Below are several short Python functions. For each one: 

- What is the domain? (What inputs are *allowed* by the system, versus which ones make the function work correctly?)
- What is the codomain? (What type does Python expect as output?)
- What is the actual range? (What outputs are actually possible?)
- For what inputs (if any) is the function undefined or problematic? 

```python
def f1(x):
    return x ** 2

def f2(x):
    return x // 2

def f3(names):
    return names[0]

def f4(x):
    if x >= 0:
        return x
    else:
        return -x

def f5(grades):
    return sum(grades) / len(grades)

def f6(x, y):
    return x + y

def f7(x, y):
    return (x + y, x - y)

def f8(s, t):
    # s and t are strings
    return s in t

def f9(nums):
    # nums is a list of integers
    return [x for x in nums if x % 2 == 0]

def f10(d):
    # d is a dictionary
    return list(d.keys())

def f11(x, y, z):
    return max(x, y, z)

def f12(func, value):
    # func is itself a function, value is a number
    return func(value) + 1

def f13(points):
    # points is a list of (x,y) tuples
    return [(y, x) for x, y in points]
```


## Codomains of these functions 

| Function | Codomain | 
| ---- | ----- | 
| `f1` |  $\{x \in \mathbb{R} : x \geq 0\}$  | 
| `f2` |   | 
| `f3` |   | 
| `f4` |   | 
| `f5` |   | 
| `f6` |   | 
| `f7` |   | 
| `f8` |   | 
| `f9` |   | 
| `f10` |   | 
| `f11` |   | 
| `f12` |   | 
| `f13` |   | 