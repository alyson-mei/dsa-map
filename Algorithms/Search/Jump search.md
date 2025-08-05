Complexity: $O(\sqrt{n})$

```python
import math

def jump_search(array, target):
	n = len(array)
	step = int(math.sqrt(n))
	prev = 0

while prev < n and array[min(step, n) - 1] < target:
	prev = step
	step += int(math.sqrt(n))
	if prev >= n:
		return -1

for i in range(prev, min(step, n)):
	if array[i] == target:
		return i


return -1
```
