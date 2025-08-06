[Colab link](https://colab.research.google.com/drive/1oWQeN-t6_sIJlup8Qv30BXeWkKfOuDCe?usp=drive_link)

Complexity: $O(n^2)$

```python
def insertion_sort(array):
	for i in range(1, len(array)):
		for j in range(i, 0, -1):
			if array[j] < array[j-1]:
				array[j], array[j-1] = array[j-1], array[j]
			else:
				break
return array
```