## 1. Basic definitions

- **Height** of a node - number of **edges** on the longest downward path from the node to a leaf
- **Depth** - number of edges from the node to the tree's root node
- **Diameter** - length of the longest path between any two nodes

## 2. Traversals
- Pre-order, in-order, post-order
- Level order

## 3. Basic problems

### 3.1. Important


- Height of a binary tree
```python
not node => return -1
return max(height(node.left), height(node.right)) + 1
```

- Same tree
```python
not node1 or not node2 => return node == node2
return node1.val == node2.val and same(node1.left, node2.left) and same(node1.right, node2.right)
```

- Diameter
```python
not node => return (0, 0)
nh_left, diam_left = rec(node.left)
nh_right, diam_right = rec(node.right)
nh = max(nh_left, nh_right) + 1
diam = max(h_left + h_right, diam_left, diam_right)
return nh, diam
```

- Path to a node

### 3.2. Not that important