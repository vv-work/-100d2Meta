# #100d2Meta 

## Sit in front of Meta HQ 

- [ ] A Create Social Media webpage 
	- [ ]  Create TikTok/Shorts Explaining what I am doing.
- [ ] A QR Code 
- [ ] A good Meta Level CV 
- [ ] A giant sign help me get job at Meta. 
- [ ] B dress nicely 

My plan is to get into meta in 100 days. 

## Todo 

- [ ] Made an implementation intention video 
- [ ] Redraw my brain map 



## Goals 
- [ ] 🔺 Reading hard Book everyday 
	- [ ] **Cracking Coding Interview** 
	- [ ] System Design by Alex Yu
- [ ] 🔺  Create `shorts` everyday
	- [ ] About my path and my chelanges 
- [ ] 🔺 Solve 3 LeetCode everyday 
	- [ ] 1 Daily leet

## Code snippets

### Binary Search 
```python
def fn(arr,target):
	l,r = 0,len(arr)-1
	
	while l<r:
		mid = l + (l-r)//2
		if arr[mid] == target:
			# We do something
			return
		elif arr[mid]>target:
			r = mid-1
		else:
			l = mid+1 
```

### Sliding Window Dynamic 

> ❗️ length of window is `r-l+1` 🚫 `r-l`

```python
def fn(arr:int[])->int:
	l = 0 
	for r in range(len(arr)):
		while CONDITION_HAPPENS:
			l+=1
		# Do some logic
```
## LC Tricks

- Normalize by sorting
```python
def signature(x:int)->str:
	return "".join(sorted(str(x)))
```

- Getting all `x^2` power of **2**
```python
for i in range(31):
	if count_digits(1 << i) == target:
		return True
```

####  Counting prime numbers (Sieve of Erastothnes)
 > [Count prime numbers LC Link](https://leetcode.com/problems/count-primes/editorial/)
```python
class Solution:
    def countPrimes(self, n: int) -> int:
        if n <= 2:
            return 0

        # Initialize numbers[0] and numbers[1] as False because 0 and 1 are not prime.
        # Initialze numbers[2] through numbers[n-1] as True because we assume each number
        # is prime until we find a prime number (p) that is a divisor of the number
        numbers = [False, False] + [True] * (n - 2)
        for p in range(2, int(sqrt(n)) + 1):
            if numbers[p]:
                # Set all multiples of p to false because they are not prime.
                for multiple in range(p * p, n, p):
                    numbers[multiple] = False

        # numbers[index] will only be true where index is a prime number
        # return the number of indices whose value is true.
        return sum(numbers)
```

### **📊 Complexity**

- **Time**: O(n log log n) (very efficient for large n)
    
- **Space**: O(n) (need a boolean array to track “crossed” numbers)
### Heap 

### Soring 

```python
sorted_dict = dict(sorted(my_dict.items(), key=lambda item: item[1], reverse=True))
```



## Memento 

### Todo 

- [ ] Add Character operations `ord()` `[]*26`
- [ ] Making Arrays [`x for x in range(N) if x%0`]

### Python

#### Notes 

>python Cycles are slow
```python
```python
import timeit

def sum1():
    s = 0
    for i in range(1000000):
        s += i
    return s

def sum2():
    return sum(range(1000000))

print 'For Loop Sum:', timeit.timeit(sum1, number=10)
print 'Built-in Sum:', timeit.timeit(sum2, number=10)

# Prints:
# For Loop Sum: 0.751425027847
# Built-in Sum: 0.266746997833
```
```

### list generation

```python
arr = [n := n // 2 for _ in range(int(math.log2(n)) + 1)]
```

#### geting input 

```python
n = int(input().strip())
```

- `input()` - getting input from terminal
- `strip()` - getting read of
#### str to list
```python
# string to list
s = “text”
arr = list(s)
# list to string
chars = [‘H’,’e’,’l’,’l’,’o’]
s = “”.join(chars)

```

## is Alpha Numerical

```python
print("3".isalnum())  # True
print("_".isalnum())  # False

```

```csharp
        Console.WriteLine(Char.IsLetterOrDigit('3')); // True
        Console.WriteLine(Char.IsLetterOrDigit('_')); // False
```

### Sorting array 
```csharp

int[] nums = int[]{5,3,4,2,1};
Array.Sort(nums);

```

## Math

```python
abs(-5) #5
```

##  LC Questions for Video 

- A [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/ )
- A [Count Prime numbers (Sieve of Erastothnes)]([238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/))
- A [334. Increasing Triplet Subsequence](https://leetcode.com/problems/increasing-triplet-subsequence/)
- A0  [Best time buy and sell stock ](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/description/)

## LC Quize 

#### [424. Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/)
> `max_freq` not key 