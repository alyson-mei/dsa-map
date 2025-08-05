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