Complexity: $O(n \log n)$

```python
def merge(array, left, mid, right): # left..<mid, mid..<right
    merged = []
    l = left
    r = mid

    while l < mid and r < right:
        if array[l] <= array[r]:
            merged.append(array[l])
            l += 1
        else:
            merged.append(array[r])
            r += 1
    
    while l < mid:
        merged.append(array[l])
        l += 1
    while r < right:
        merged.append(array[r])
        r += 1

    array[left:right] = merged

def merge_sort(array, left=0, right=None):
    if right is None:
        right = len(array)
    if right - left <= 1:
        return array
    
    mid = (right + left) // 2
    merge_sort(array, left=left, right=mid)
    merge_sort(array, left=mid, right=right)
    merge(array, left, mid, right)

    return array
```