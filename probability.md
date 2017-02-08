

```python
import random

red_count = 0 
for i in range(10000):
    if random.random() < 2/3:
        red_count += 1
print("Red: ", red_count)
```

    Red:  6618
    


```python
import random

blue_count = 0 
for i in range(10000):
    if random.random() < 1/3:
        blue_count += 1
print("Blue: ", blue_count)
```

    Blue:  3286
    


```python
import random

random.random()
```




    0.4956090437345919



### possible events

[r,r]
[r,b]
[b,r]
[b,b]

with replacement the probilities dont change
without replacement they do

probsbility of red first is 8/12
probability of blue first is 4/12

probability of red having selected a red first is 7/11

probability of [r,r] iis (8/12) * (7/11)-> 56/132


```python
if random.random() < 8/12:
    print("The first marbel was red")
```

    The first marbel was red
    


```python
for i in range(10):
    if random.random() < 8/12:
        print("The first marbel was red")
```

    The first marbel was red
    The first marbel was red
    The first marbel was red
    The first marbel was red
    The first marbel was red
    The first marbel was red
    The first marbel was red
    The first marbel was red
    


```python
# int num_red
num_red = 0
for i in range(10):
    if random.random() < 8/12:
        num_red += 1

print(num_red)
```

    7
    


```python
num_red = 0
for i in range(100000):
    if random.random() < 8/12:
        num_red += 1

print(num_red/100000)
```

    0.66779
    


```python
num_interns = 10
num_red = 0
for i in range(num_interns):
    if random.random() < 8/12:
        num_red += 1
print(num_red/num_interns)
```

    0.6
    


```python
iterations = 100000
num_red = 8
num_marbles = 12
red_count = 0
for i in range(iterations):
    if random.random() < num_red/num_marbles:
        red_count += 1
print(red_count/iterations)

```

    0.6682
    


```python
iterations = 100000
num_red = 8
num_marbles = 12
red_count = 0
for i in range(iterations):
    if random.random() < num_red/num_marbles:
        if random.random() < (num_red - 1) / (num_marbles - 1):
            red_count += 1
print(red_count/iterations)
```

    0.42362
    


```python
56/132
```




    0.42424242424242425



### write code that models getting [B,B]


```python
iterations = 100000
num_blue = 4
num_marbles = 12
blue_count = 0
for i in range(iterations):
    if random.random() < num_blue/num_marbles:
        if random.random() < (num_blue - 1) / (num_marbles - 1):
            blue_count += 1
print(blue_count/iterations)
```

    0.09032
    


```python
(4/12) * (3/11)
```




    0.0909090909090909




```python
# prbability of picking [R,B]

iterations = 100000
num_red = 8
num_blue = 4
num_marbles = 12
blue_count = 0
red_count = 0
for i in range(iterations):
    if random.random() < num_red/num_marbles:
        if random.random() < (num_blue) / (num_marbles - 1):
            blue_count += 1
            red_count += 1
print(blue_count/iterations)
```

    0.24361
    


```python
(4/12) * (8/11)
```




    0.24242424242424243




```python
# prbability of picking [B,R]

iterations = 100000
num_red = 8
num_blue = 4
num_marbles = 12
blue_count = 0
red_count = 0
for i in range(iterations):
    if random.random() < num_blue/num_marbles:
        if random.random() < (num_red) / (num_marbles - 1):
            blue_count += 1
            red_count += 1
print(red_count/iterations)
```

    0.23964
    


```python
(8/12) * (4/11)
```




    0.24242424242424243




```python

```
