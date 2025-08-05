```python
def binary_search(array, target):
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
target = 7
array = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
# 

```


