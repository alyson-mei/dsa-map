[Colab link]()

```python
def binary_search_a(array, target):
	if not array:
		return -1
		
	l = 0
	r = len(array) - 1
	while r > l + 1:
		m = (r + l) // 2
		if array[m] < target:
			l = m
		else:
			r = m
	if array[l] == target:
		return l
	elif array[r] == target:
		return r
	else:
		return -1
```

It works, but it's not a standard way to implement a binary search. It's intuitive for a simple case, but doesn't work that well when we search for some condition

Example to make a standard way more intuitive:
```python
target = 6
array = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
# 0)     l           m              r
# Note that this is enough to search in array[5<=...<=9] now
# because array[m] < target 
# 1)                    l     m     r  
# New search in array[5<=...<=6]
# 2)                   l,m  r
# New search in array[6<=...<=6]
# 3)                     l,m,r   
```

```python
def binary_search_b(array, target):
	l = 0
	r = len(array) - 1
	while l <= r:
		m = (l + r) // 2
		if array[m] < target:
			l = m + 1
		elif array[m] > target:
			r = m - 1
		else:
			return m
	return -1 
```