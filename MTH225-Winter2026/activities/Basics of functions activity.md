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
| `f1` |  $\mathbb{R}$  | 
| `f2` |  $\mathbb{Z}$ | 
| `f3` |  Whatever the data type of `names` entries is | 
| `f4` |  $\mathbb{R}$ | 
| `f5` | $\mathbb{R}$  | 
| `f6` | $\mathbb{R}$  | 
| `f7` | $\mathbb{R} \times \mathbb{R}$  | 
| `f8` | Booleans ($\\{True, False\\}$)  | 
| `f9` | Set of all lists   | 
| `f10` |  Set of all lists | 
| `f11` | $\mathbb{R}$  | 
| `f12` |  *Skip this one* | 
| `f13` | Set of all lists  | 