[Colab link](https://colab.research.google.com/drive/1R0PGiA_5jlXIu9Rg4g7muxN0y-x8Unwt?usp=sharing)

Complexity: $O(n)$

```python
def linear_search(array, target):
	for i in range(len(array)):
		if array[i] == target:
			return i
	return -1
```