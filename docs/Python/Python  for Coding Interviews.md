**I am not a Python expert**. I am a web developer and have been using mostly JavaScript and TypeScript in my past work experience. However, I use Python for my coding interviews. Its concise syntax and dynamic typing (a blessing and a curse 😅) make it perfect for quickly writing solutions to coding problems under pressure. 

This document should serve as a **quick guide to Python**, introducing you to the syntax and basic components that you’d need when using Python for coding interviews. It is **not a comprehensive** guide to Python, you’d need more than this to build an entire software with Python. 

> **Resource:** [Neetcode](https://www.youtube.com/watch?v=0K_eZGS5NsU) (highly recommend this channel)
## 1. Variables
Python is a **dynamically typed** programming language, so **data type is determined at run time**. That’s why unlike other statically typed languages like C++ or Java, you don’t need to declare the data type, at all!
```python
n = 0 # no need to specify data type 
print("n =", n) 
>>> n = 0

n = "abc" # reassigned data type to string
print("n =", n)
>>> n = abc

# multiple assignments. 
# syntax: variable1, variable2 ...: value1, value2, ...

n, m, z = 0.125, "abc", False

print("n =", n)

print('m =', m)
```

**Incrementing** in Python is a little bit different: 
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
## 2. Conditional Statements
Python doesn't use parentheses or curly braces. Instead, it relies on **indentation** to define code blocks. This syntax may be confusing for beginners (it definitely was for me 😅).
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
## 3. Loops
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
## 4. Math
```python
# division is decimal by default
print(5 / 2)
>>> 2.5

# double slash rounds DOWN
print(5 // 2)
>>> 2

# NOTE: round DOWN not towards 0
print(-3 // 2) # -1.5, but gets rounded DOWN to -2, not UP to -1
>>> 2 

# to round towards zero
# use decimal division then convert to int
print(int(-3 // 2))
>>> 1
```