
## Todo 

- [ ] `defaultdict(int)`  what it is and how to use it ?
- [ ] `chr` magic and 

```python
from collections import Counter
import heapq

  
class Solution:
	def topKFrequent(self, nums: List[int], k: int) -> List[int]:
	
		count = Counter(nums)
		return heapq.nlargest(k,count.keys(),key=count.get)
```

## Memoization through cache

```python
# memoization in Python 
@lru_cache(maxsize=None)
def min_path(row, col):
```

## Sliding window 
## input
### input-> int 

```python
N = int(input().strip())
```

### input->arr

```python
arr = list(int,map(input().strip().split()))
```

> In Python, the built-in **map()** function applies a function to every item in an `iterable` (like a list, tuple, or string) and returns an _iterator_ with the results.


## Chars

```python
c = 'a'
c.isalnum()
c.isupper() # is upper case
c.islower()
```

## Methods 

`map()` - maps method to the each element of `iteratable` 

```python
words = ["hello", "world"]
uppercased = map(str.upper, words)

print(list(uppercased))  # ['HELLO', 'WORLD']

# Other example
nums = [1, 2, 3, 4]
squared = map(lambda x: x**2, nums)

print(list(squared))  # [1, 4, 9, 16]
```
