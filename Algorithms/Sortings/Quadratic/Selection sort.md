[Colab link](https://colab.research.google.com/drive/1uZCKEuAVNR-GpOteD4cJU3EWWFBlAQaz?usp=drive_link)

Complexity: $O(n^2)$

```python
def selection_sort(array):
	for i in range(len(array)-1):
		min_id = i
		for j in range(i+1, len(array)):
			if array[j] < array[min_id]:
				min_id = j
		array[min_id], array[i] = array[i], array[min_id]
	return array
```