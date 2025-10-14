---
title: Advanced Algorithms
updated: 2025-10-12 14:19:18Z
created: 2025-09-26 07:53:46Z
latitude: 12.97159870
longitude: 77.59456270
altitude: 0.0000
---

# Dynamic Programming
## Difference between DP and Divide & Conquer
|Divide & Conquer|Dynamic Programming|
|:-----------:|:------:|
|Subproblem overlapping is mostly independent|Subproblem overlap significantly|
|Divide Problem; solve subproblem; combine recursively|solve & store subproblem; reuse results|
|tabulation not used / not required|tabulation required|
|Recursion tree with redundant work|Avoid redundant work by caching|

## Fibonacci 
> by traditional method
> takes $\text O(2^n)$ time
```c
int fibb(n){
	//accepts n>=0
	if (n==0 || n==1)
		return n;
	return  fibb(n-1) + fibb(n-2)
}
```

> By DP

```c
int fibb (n, memo={}){
	if (n in memo)
		return memo[n];
	if n<=1 //i.e. 1 or 0
		return n;
	memo[n] = fibb(n-1, memo) + fibb(n-2, memo)

		return memo[n]
}
```

## Rodcutting Problem
Given a rod of length `n` and an array `price[]`. `price[i]` denotes the value of a piece of length `i`.

The task is to determine the maximum value obtainable by cutting up the rod and selling the pieces.

```c
r[n] = max(p[i] + r[n-i]) //from i = 1 to n
cut_rod (p,n)
	if (n==0)
		return 0;
	q = -inf;
	for (i=1 to n)
		q = max(q, p[i]+cutrod(p,n-i));
	return q
```

### Rodcutting by DP:
1) Top Down

```python
#Memoized version from CLRS
def Memoized_Cut_Rod(p, n):
	r = [-inf]*(n+1) # table for memorization
	return Memoized_Cut_Rod_Aux(p, n, r)

def Memoized_Cut_Rod_Aux(p, n, r):
	if r[n]>=0: #already solved
		return r[n]
	if n==0:
		q=0
	else:
		q=-inf
		for i in range(1, n+1):
			q = max(q, p[i]+Memoized_Cut_Rod_Aux(p, n-i, r))
	r[n]=q
	return q
```

2) Bottom Up

```cpp
Bottom_Up_Cut_Rod(p, n)
	let r[0..n] be a new array
	r[0] = 0
	for j = 1 to n
		q = -inf
		for i = 1 to j
			q = max(q, p[i]+r[j-i])
		r[j]=q
	return r[n]
```

## String Matching Problem
Given two strings, `text` and `pattern`, find the first occurence of `pattern` in `text`.
>Brute Force Algorithm.
>Takes $\text O(n^2)$ time.
```
for i=0 to n-m{
	for j=0 to m-1{
		if (text[j] != pattern[i])
			break;
		if (j=m-1)
			return i;
	}
return -1;
}
```

>Boyer-Moore Algorithm
>Not covered here

## Longest Common Subsequence Problem
Given two string `string1` and `string2`, you are tasked with finding the longest string that can be obtained from `string1` and `string2` by deleting elements.

```
//Example
string1 = "thoughtful"
string2 = "shuffle"

//Output
LCS = "hufl"
```

>Using Dynamic Programming:

- For every prefix of `string1` and prefix of `string2`, we'll compute the length `l` of an LCS.

<font color=red>continue later from ppt pg 14</font>