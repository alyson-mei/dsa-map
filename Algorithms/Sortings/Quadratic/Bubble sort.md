[Colab link](https://colab.research.google.com/drive/1xUoPeNPd-GhI_SXcWDWaPv5YiYNn_ph5?usp=drive_link)

Complexity: $O(n^2)$

```python
def bubble_sort(array):
	for i in range(len(array)-1):
		for j in range(len(array)-1-i):
			if array[j] > array[j+1]:
				array[j], array[j+1] = array[j+1], array[j]
	return array
```