202402070137
# Common Time Complexity Equations

## Notes

Time complexity can be rendered from the inner most statement of nested scopes since it will be the statement that is ran the most

```C++
for(int i=0; i<n; i++) {
	statement;
}

// O(n) Time
```
- Each iteration is incremented by 1 until n which means it will take n times to reach termination
```C++
for(int i=n; i>0; i--) {
	statement;
}

// O(n) Time
```
- Same as above except in reverse
```C++
for(int i=1; i<n; i += 2 or 20) {
	statement;
}

// O(n) Time
```
- Even though the increment is larger it is still additive which will execute n amount of times until termination
```C++
for(int i=0; i<n; i++) {
	for(int j=0; j<n; j++) {
		statement;
	}
}

// O(n2) Time
```
- The inner loop will be executed up to n times since that is the terminator of the outer loop
- Then subsequentially the inner loop will execute its statement(s) n times resulting in exponential time n$^2$
```C++
for(int i=0; i<n; i++) {
	for(int j=0; j<i; j++) {
		statement;
	}
}

// O(n2) Time
```
- Outer loop will execute the inner loop n times
- Inner loop, according to the sum of natural numbers formula, will equate to n(n+1)/2
- Simplifying this formula we get a degree of 2 which derives a time complexity of n$^2$
```C++
int p = 0
for(int i=1; p<=n; i++) {
	p += i; 
}

// O(sqrt(n)) Time
```
- Because of the sum of natural numbers formula p's time complexity is k(k+1)/2
- Since it needs to be in terms of n (n = k(k+1)/2) simplified n = k$^2$ which would be $\sqrt{n}$ making that the time complexity
```C++
for(int i=1; i<n; i *= 2) {
	statement;
}

// O(log(n)) Time
```
- Since the loop will increase multiplicatively by 2 it will run 2$^k$ times
- In terms of n that will be n = 2$^k$ which simplified will give us time complexity of log$_2$ (n) or just log(n) since the base is a constant and has minimal significance to performance
```C++
for(int i=n; i>=1; i /= 2) {
	statement;
}

// O(log(n)) Time
```
- Reverse of above
- n/2$^k$ = 1 which simplifies to n = 2$^k$ same as above which we know it log$_2$ (n)
```C++
for(int i=0; i*i<n; i++) {
	statement;
}

// O(log(n)) Time
```
- Terminating statement implies i$^2$ = n which in turn simplifies to $\sqrt{n}$ our time complexity
```C++
for(int i=0; i<n; i++) {
	statement;
}
for(int j=0; j<n; j++) {
	statement;
}

// O(n) Time
```
- Even though there are 2 for loops here since one is not nested in the other they both execute at n times which results in a time complexity O(n)
```C++
p=0
for(int i=1; i<n; i*=2) {
	p++;
}
for(int j=1; j<p; j*=2) {
	statement;
}

// O(log(log(n))) Time
```
- The second loop will be a time complexity of log(p)
- the first loop will be a complexity of log(n) which is equal to p since it is determinate of the termination of that first for loop
- Hence p = log(n) replacing the original p in log(p) we will get log(log(n))
```C++
for(int i=0; i<n; i++) {
	for(int j=1; j<n; j*=2) {
		statement;
	}
}

// O(n) Time
```
- The outer loop is determined to be O(n) while the inner loop is log(n)
- since the inner loop runs at the time complexity of the outer those 2 combined will derive a total time complexity of n log(n)

---
## Links

- [[Time Complexity]]
- [[Sum of  n Natural Numbers Formula]]

---

## Source

- [Bari's Algorithm Playlist 1.5.2](https://youtu.be/9SgLBjXqwd4?si=ivqdZZ1Kb6mXiuJm)