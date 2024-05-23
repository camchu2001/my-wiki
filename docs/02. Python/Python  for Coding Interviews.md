This document should serve as a **quick guide to Python**, introducing syntax and basic components that one would need when using Python for coding interviews.

> **Resource:** [Neetcode](https://www.youtube.com/watch?v=0K_eZGS5NsU)
### 1. Variables
Python is a **dynamically typed** programming language, so **data type is determined at run time**. That’s why unlike other statically typed languages like C++ or Java, you don’t need to declare the data type, at all!
```python
n = 0 # no need to specify a data type 
print("n =", n) 
>>> n = 0

n = "abc" # reassigned data type to string
print("n =", n)
>>> n = abc

# multiple assignments. 
# syntax: variable1, variable2 ...: value1, value2, ...

n, m, z = 0.125, "abc", False

print("n =", n)
print("m =", m)
print("z =", z)
```

**Incrementing** in Python is a little bit **different**: 
```python
n = n + 1 # good
n+= 1     # good
n++       # syntax error -> cannot be done
```

Python doesn’t use `null` for an absence of value, it uses **`None`**. 
```python
n = 4
n = None
print("n =", n) 
>>> n = None
```
### 2. Conditional Statements
Python doesn't use parentheses or curly braces. Instead, it relies on **indentation** to define code blocks.
```python
n = 1
if n > 2:
  n-= 1 # this code belongs to the if block
elif n == 2: 
  n *= 2 # this code belongs to the elif (else if) block
else: 
  n +=2 # this code belongs to the else block
```

* **`and` = `&&`**
* **`or` == `||`**
```python
# parenthese are needed for multi-line conditions
n, m = 1, 2
if ((n > 2 and
  n != m) or n == m):
  n += 1
```
### 3. Loops
```python
# while loops are relatively straightforward
n = 0
while n < 5: 
  print(n) 
  n += 1 
>>> 0 1 2 3 4

# for loops usually utilizes the range() function
# loop from i = 0 to i = 4, 5 is not included
for i in range(5): 
  print(i)
>>> 0 1 2 3 4
```

* `range()` function
```python
# looping from i = 2 to i = 5
for i in range(2, 6): 
  print(i)
>>> 2, 3, 4, 5

# looping in reverse, from i = 5 to i = 2
for i in range(5, 1, -1):
  print(i)
>>> 5, 4, 3, 2
```
### 4. Math
* **Division**: 
```python
# division is decimal by default
print(5 / 2)
>>> 2.5

# double slash rounds DOWN
print(5 // 2)
>>> 2

# NOTE: round DOWN not towards 0
print(-3 // 2) # -1.5, but gets rounded DOWN to -2, not UP to -1
>>> -2 

# to round towards zero
# use decimal division then convert to int
print(int(-3 / 2))
>>> -1
```

* **Mod**: 
```python
# similar to most languages
print(10 % 3)
>>> 1

# different wtih negative values
# this can be confusing
print(-10 % 3)
>>> 2

# To be consistent with other languages modulo
import math
print(math.fmod(-10, 3))
>>> -1.0
```

* **Other math helpers**: 
```python
print(math.floor(3 / 2))
>>> 1

print(math.ceil(3 / 2))
>>> 2

print(math.sqrt(4))
>>> 2.0

print(math.pow(2, 3))
>>> 8.0
```

* **Max, Min integer:** 
```python
float("inf") # max
float("-inf") # min

# Python numbers are infinite so they never overflow
print(math.pow(2, 200))
>>> 1.6069380442589903e+60

# But still less than infinity
print(math.pow(2, 200) < float("inf"))
>>> True
```
### 5. Arrays - Lists
```python
arr = [1, 2, 3] # declare
print(arr)
>>> [1, 2, 3]
```
* Python’s arrays are dynamic, so they can be used as a **stack**. The **`append()` and `pop()` operations** take a time complexity of **O(1)** because it’s just inserting/removing the last index’s value.  
```python
# insert to the end
arr.append(4) 
arr.append(5)
print(arr)
>>> [1, 2, 3, 4, 5]

# remove the end value
arr.pop()
print(arr)
>>> [1, 2, 3, 4] # popped value 5
```

* **Insertion and deletion** of a value into/from a random index `ith` has an **O(n)** complexity because it needs to shift all the other elements to the right/left: 
```python
# insert a value to a specific index
arr.insert(1, 7) # inserting 7 to index 1
arr.insert(6, 7) # inserting 7 to index 6, even if 6 is out of bound it works
print(arr)
>>> [1, 7, 2, 3, 4, 7]

# remove the first occurrence of a value from the array
arr.remove(7) # removing element 7 from the array
print(arr)
>>> [1, 2, 3, 4, 7]
```

* **Accessing/reassigning** the value of an array’s index is **O(1)** time complexity:
```python
arr[0] = 0
arr[3] = 0
print(arr)
>>> [0, 2, 3, 0, 7]

# negative index reads the value from the end
print(arr[-1]) 
>>> 7

print(arr[-2])
>>> 0
```

* **Initializing** an array of size n with a default value of 1:
```python
n = 5
arr = [1] * n
print(arr)
>>> [1, 1, 1, 1, 1]

print(len(arr)) 
>>> 5
```

* **Sublists (slicing)**, the last index is non-inclusive: 
```python
arr = [1, 2, 3, 4]
print(arr[1:3])
>>> [2, 3] # doesn't include 3rd index

print(arr[0: 4])
>>> [1, 2, 3, 4]
```

* **Unpacking** assignment allows assigning the elements of a list (or any iterable) to multiple variables in a single statement. 
```python
# the number of variables = number of elements in the array
a, b, c = [1, 2, 3]
print(a, b, c)
>>> 1 2 3
```

* **Looping through an array**: 
```python
nums = [1, 2, 3]

for i in range(len(nums)):
  print(nums[i])
>>> 1 2 3

# you can do the same operation without using index
for num in nums: 
  print(num)
>>> 1 2 3

# print both index and value
for i, n in enumerate(nums)
  print(i, n)
>>> 0 1
>>> 1 2
>>> 2 3
```

* **Looping** through multiple arrays simultaneously with **unpacking** and **`zip()` function**. `zip()` combines the elements from `list1` and `list2` into tuples, pairing up the corresponding elements
```python
nums1 = [1, 3, 5]
nums2 = [2, 4, 6]
zipped = zip(nums1, nums2)

for element in zipped:
  print(element)
>>> (1, 2)
>>> (3, 4)
>>> (5, 6)

for n1, n2 in zip(nums1, nums2): 
  print(n1, n2)
>>> 1 2
>>> 3 4
>>> 5 6
```

* **Reverse an array:**
```python
nums = [1, 2, 3]
nums.reverse()
print(nums)
>>> [3, 2, 1]
```

* **Sorting an array**, the default is ascending order: 
```python
arr = [5, 4, 23, 1, 0, 8]
arr.sort()
print(arr)
>>> [0, 1, 4, 5, 8, 23]

# sort in descending order
arr.sort(reverse = True)
print(arr)
>>> [23, 8, 5, 4, 1, 0]

# sorting an array of strings - alphabetical order by default
arr = ["billy", "zeke", "keith", "cece", "annabeth"]
arr.sort()
print(arr)
>>> ["annabeth", "billy", "cece", "keith", "zeke"]

# custom sort (by length of string)
arr.sort(key=lambda x: len(x))
print(arr)
>>> ["cece", "zeke", "billy", "keith", "annabeth"]
```

* **List comprehension**, a more advanced way to initialize lists: 
```python
arr = [i for i in range(5)]
print(arr)
>>> [0, 1, 2, 3, 4]

arr = [i+i for i in range(5)]
print(arr)
>>> [0, 2, 4, 6, 8]
```

* **2-D Lists**: 
```python
# declare a 2D array
arr = [[0] * 3 for i in range(4)]
print(arr)
>>> [[0, 0, 0], [0, 0, 0], [0, 0, 0], [0, 0, 0]]

arr[0][1] = 2
print(arr)
>>> [[0, 2, 0], [0, 0, 0], [0, 0, 0], [0, 0, 0]]

# however, this syntax won't work
arr = [[0] * 4] * 4
print(arr)
>>> [[0, 0, 0], [0, 0, 0], [0, 0, 0], [0, 0, 0]]

# it's the same list is replicated 4 times, not 4 different lists
# -> when you modify one inner list, you end up modifying all of them
arr[0][1] = 2
print(arr)
>>> [[0, 2, 0], [0, 2, 0], [0, 2, 0], [0, 2, 0]]
```
### 6. Strings
```python
s = "abc"

# we can performing slicing on strings
print(s[0:2])
>>> "ab"
```
* Strings are **immutable**, so we cannot change individual characters of a string. However, we can **update** a string. Because this operation creates a new string, it has a complexity of **O(n)**. 
```python
# strings are immutable 
# attempting to reassign a part of the string will raise an error
s[0] = "A"
print(s)

# we can update a string, this creates a new string "abcdef
s+= "def"
print(s)
>>> "abcdef"
```

* Numeric strings can be converted into integers using `int()` and numbers can be converted to strings, using `str()`.
```python
# adding two numbers
print(int("123") + int("123"))
>>> 246

# adding two strings
print(str(123) + str(123))
>>> 123123
```

* You can get the ASCII value of a character using `ord()`: 
```python
print(ord("a"))
>>> 97

print(ord("b"))
>>> 98
```

* You can join a list of strings with `join()`. 
```python
# syntax for join() method
string = delimiter.join(iterable)
```
- `delimiter`: The string that will be **inserted between each element** of the iterable. It can be an empty string `''`, a single-character, or a multi-character string.
- `iterable`: The iterable whose elements will be concatenated into the string.

```python
my_list = ['apple', 'banana', 'orange']
result = "".join(my_list)
print(result)
>>> applebananaorange

result = ", ".join(my_list)
print(result)
>>> apple, banana, orange
```
### 7. Queues
A queue is a data structure that follows the **First-In-First-Out (FIFO)** principle. In a queue, elements are inserted at the end (enqueue operation) and removed from the front (dequeue operation).

**Queue** is a data type in Python, but it's not a built-in data type like lists or dictionaries. Instead, it's typically implemented using the `queue` module in Python's standard library. Queues in Python are **double-ended queues** by default, allowing efficient insertion and deletion at both ends.
1. **`append(x)`**: Adds element `x` to the right end of the `deque`.
2. **`appendleft(x)`**: Adds element `x` to the left end of the `deque`.
3. **`pop()`**: Removes and returns the rightmost element (the last element) from the `deque`.
4. **`popleft()`**: Removes and returns the leftmost element (the first element) from the `deque`.
```python
# imports the `deque` class from the `collections` module. `deque` stands for "double-ended queue"
from collections import deque

# creates an empty double-ended queue named `queue`
queue = deque()

# append elements `1` and `2` to the right end of the queue
queue.append(1) 
queue.append(2)
print(queue)
>> [1, 2]

# removes and returns the leftmost element
queue.popleft()
print(queue)
>>> [2]

# appends the element `1` to the left end of the queue
queue.appendleft(1)
print(queue)
>>> [1, 2]

#removes and returns the rightmost element (the last element)
queue.pop()
print(queue)
>>> [1]
```
### 8. HashSet
A set is an **unordered collection of <u>unique</u> elements**. It is used to store items without duplicates and provides efficient operations for membership testing, adding, and removing elements.

```python
# Create an empty set
mySet = set()

# Add elements to the set
mySet.add(1)
mySet.add(2)

# Print the set
print(mySet)  
>>> {1, 2}

# Print the length of the set
print(len(mySet))  
>> 2

# Check if elements are in the set
print(1 in mySet)  # Output: True
print(2 in mySet)  # Output: True
print(3 in mySet)  # Output: False

# Remove an element from the set
mySet.remove(2)
print(2 in mySet)  # Output: False

# Create a set from a list
print(set([1, 2, 3]))  
>>> {1, 2, 3}

# Set comprehension
mySet = {i for i in range(5)}
print(mySet)  
>>> {0, 1, 2, 3, 4}
```