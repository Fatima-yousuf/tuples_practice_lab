# Tuples in Python – Practice Lab

## 1. Exercising Tuples

### 1a. Take five inputs from the user and save in a tuple
Example input/output:

```python
my_tuple = tuple(input(f"Enter element {i+1}: ") for i in range(5))
print("Your tuple:", my_tuple)
```
### 1b. Single element tuple
```python
single_element_tuple = (5,)
print(single_element_tuple, type(single_element_tuple))
```
### 1c. Count repeated integers
```python
my_tuple = (1, 2, 3, 4, 3, 2, 1, 2, 3, 5, 4, 3, 2, 1)
counts = {x: my_tuple.count(x) for x in set(my_tuple)}
print("Count of each integer:", counts)
```
### 1d. Concatenate tuple with itself
```python
my_tuple_d = my_tuple + my_tuple
print("Original tuple:", my_tuple)
print("Concatenated tuple:", my_tuple_d)
print("Are the objects the same?", my_tuple is my_tuple_d)
```
### 1e. Why these operations aren’t legal
```python
x = (1, 2, 3, 4)
x.append(1)      # ❌ Not allowed: tuples are immutable
x[1] = "hello"   # ❌ Not allowed: cannot change elements
del x[2]         # ❌ Not allowed: cannot delete elements
```
# Explanation:
```python
Tuples act like locked boxes, once you put something into them, you can't make changes. If you attempt to add, delete or modify any items, you will encounter an error message from Python because a tuple can never change from the time you created it.
```
### 2a. Simple tuple unpacking
```python
(one, two, three, four) = (1, 2, 3, 4)
print("one:", one, type(one))
print("two:", two, type(two))
print("three:", three, type(three))
print("four:", four, type(four))
```
### 2b. Extended unpacking with 
```python
x = (1, 2, 3, 4)
a, b, *c = x
print("a:", a)
print("b:", b)
print("c:", c)
```
### 2c. Extended unpacking with
```python
a, *b, c = x
print("a:", a)
print("b:", b)
print("c:", c)
```
### 3. Memory Management
```python
my_x = [100, 200, 300, 400]
my_y = (200, 300, 400, 500)
print("Memory addresses of my_x elements (list):")
for i in range(len(my_x)):
    print(f"Index {i}: {id(my_x[i])}")
print("\nMemory addresses of my_y elements (tuple):")
for i in range(len(my_y)):
    print(f"Index {i}: {id(my_y[i])}")
```
### Challenges:
-A challenge I faced was understanding how the fractional part of a number works.
-I also learned the importance of separating headings from code sections to keep the assignment organized and readable.
-Practicing tuples helped me understand when it is best to use immutable data versus mutable data.

