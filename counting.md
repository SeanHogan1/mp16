

```python
num_order = {'0':'1', '1':'2', '2':'3', '3':'4', '4':'5', '5':'6', '6':'7', '7':'8', '8':'9', '9':'0'}
```


```python
def symbol0():
    return sorted(num_order)[len(num_order) - 1]
```


```python
def mynext(symbol):
    if symbol == symbol0():
        return (1, symbol1())
    else:
        return (0, num_order[symbol])
```


```python
def first_c_symbol():
    return num_order[first_symbol()]
```


```python
number = [first_symbol()]
for i in range(20):
    carry = 1
    for idx, symbol in enumerate(number):
        if carry == 1:
            carry, symbol = mynext(symbol)
            number[idx] = symbol
        else:
            break
    if carry == 1:
        number.append(first_counting_symbol())
    print(''.join(number[::-1]))
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-5-f8a20e292c17> in <module>()
    ----> 1 number = [first_symbol()]
          2 for i in range(20):
          3     carry = 1
          4     for idx, symbol in enumerate(number):
          5         if carry == 1:
    

    NameError: name 'first_symbol' is not defined



```python
def symbol1():
    return sorted(num_order)[0]
```


```python
number = [symbol1()]
for i in range(20):
    carry = 1
    for idx, symbol in enumerate(number):
        if carry == 1:
            carry, symbol = mynext(symbol)
            number[idx] = symbol
        else:
            break
    if carry == 1:
        number.append(first_c_symbol())
    print(''.join(number[::-1]))
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    11
    12
    13
    14
    15
    16
    17
    18
    19
    20
    


```python

```
