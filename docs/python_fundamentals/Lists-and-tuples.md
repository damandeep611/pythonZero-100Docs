---
title: Lists and Tuples 
sidebar_position: 2

---

## Lists 
Lists are mutable and we use [ ] syntax to store values in lists
``` py
stocks = ['AAPL', 'GOOGL', 'TSLA', 'MSFT']
```
## SPAM for list operations - sort, pop, append, modify

### sort - sort list items 
```py
numbers = [1,5,6,2,8,9,3,5,7]
numbers.sort()
print(numbers)
```


### pop -  removes the last item in the list
```py
heros = ['flash', 'batman', 'supe', 'martian']
heros.pop()
print(heros)
```


### apped - adds a item at the end 
```py
heros.append('shazam')
print(heros)
```


### modify - modify the items in the list 
```py
heros[2] = 'superman'
print(heros)
```



## Tuples 
Tuples are immutable, their values can't be changed, these are used when we have to keep uniformity in values,
```py
location = (89.8292, 82.1819)
```


## Key differences between lists and tuples
one of the key difference between lists and tuples is that lists are mutable and are used where you need to make lot of changes to the lists elements, and while tuples are used when you have to keep the data constant . i.e when using cordinates etc

### common list and tuple operations 

### finding length 
```py
print(len(numbers))
```


### indexing 
```py
print(heros[1])
```


### slicing  - prints the numbers between the mentioned indexes
```py
print(numbers[2:6])
```


### concatenation 
```py
listOne = [1,2] + [44, 66]
tupleOne = (2,3) + (31, 32)
print(f"this is list concatenation: {listOne}, and this is the tuple concatenation: {tupleOne}")
```
