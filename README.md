# python-for-leetcode

Python tricks that will help you with leetcode

## Tricks

1. Use Python 3

2. One-liner Trie

```python
trie = lambda :defaultdict(trie)
trie = trie()
```

[Implement trie prefix tree](https://leetcode.com/problems/implement-trie-prefix-tree/)

3. Flatten 2D array (matrix)

```python
a = [
  [1,2,3],
  [4,5,6],
  [7,8,9]
]

print(sum(a), [])
```

4. Reverse a list or string

```python
str = "abcde"
print(str[::-1])

a = [1, 2, 3, 4, 5]
print(a[::-1])
```

5: Array index trick (e.g. Palindrome checking)

```python
# Before
str = "abcba"
n = len(str)
print(all(str[i] == str[n-i-1] for i in range(n)))

# After
str = "abcba"
print(all(str[i] == str[~i] for i in range(len(str))))
```

6. Tuple unpacking

7) Boolean as int

8) map

9) redeuce

10) Copy list

```python
a = [1, 2, 3]
b = a[:]
```

11. Dictionary defualt value

```python
# Before
d = {}  # dictionary of list
if k in d:
    d[k].append(v)
else:
    d[k] = [v]

# After

# 1. setdefault method on dict
d = {}  # dictionary of list
d.setdefault(k, []).append(v)

# 2. collections.defaultdict
d = collections.defaultdict(list)
d[k].append(v)
```

12. Swap variables

```python
a, b = b,a
```

13. Chained boolean comparisons

```python
if 1 < 2 < 3:

if 'a' < 'c' > 'b':

if 1 == True != False:
```

Todo:

- zip
- float("inf")
- itertools.zip_longest
- collections.Counter
- heapq
- list as queue
- collections.deque as stack
- string.split
- itertools.chain
- yield in recursion
- sort vs sorted
- sort tuple, sort by key
- range vs xrange
- string.join
- bisect
- list initialzation (using asterisk and anti-pattern)
- enumerate
- Fix markdown syntax
- Add example problems to each trick

## Reference

- https://github.com/brennerm/PyTricks
- Leetcode problem discussions (especially comments from Stefan Pochmann)
