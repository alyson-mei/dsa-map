[Colab link](https://colab.research.google.com/drive/1TFlLaw7HmBJL9xf4UVdFnZBomXSj43bv?usp=sharing)

Complexity: $O(n \log n)$

```python
import random

def partition(array, left, right):
    pivot_ind = random.randint(left, right - 1)
    array[pivot_ind], array[right - 1] = array[right - 1], array[pivot_ind]
    pivot = array[right - 1]

    p = left
    for i in range(left, right - 1):
        if array[i] <= pivot:
            array[p], array[i] = array[i], array[p]
            p += 1
    
    array[p], array[right - 1] = array[right - 1], array[p]
    return p

def quicksort(array, left=0, right=None):
    if right is None:
        right = len(array)
    if right - left <= 1:
        return array
    
    p = partition(array, left, right)
    quicksort(array, left, p)
    quicksort(array, p + 1, right)
    return array

```