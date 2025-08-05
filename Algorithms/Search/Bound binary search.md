[Colab link](https://colab.research.google.com/drive/1x1ExCQwdfbwQNJznGrJgUdNwUGt4UahE?usp=sharing)

Complexity: $O(\log n)$

```python
def lower_bound_search(array, target):
	l = 0
	r = len(array) - 1
	
	while r >= l:
		m = (r + l) // 2
		if array[m] < target:
			l = m + 1
		else:
			r = m - 1
			
	return l if l < len(array) and array[l] == target else -1
```