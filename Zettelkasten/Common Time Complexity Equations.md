202402070137
# Common Time Complexity Equations

## Notes

Time complexity can be rendered from the inner most statement of nested scopes since it will be the statement that is ran the most

```C++
for(int i=0; i<n; i++) {
	statement; // n Time
}

// O(n) Time
```

```C++
for(int i=n; i>0; i--) {
	statement; // n Time
}

// O(n) Time
```

```C++
for(int i=1; i<n; i += 2 or 20) {
	statement; // n/2 or n/20
}

// O(n) Time
```

```C++
for(int i=0; i<n; i++) {
	for(int j=0; j<n; j++) {
		statement; // n * n
	}
}

// O(n2) Time
```

```C++
for(int i=0; i<n; i++) {
	for(int j=0; j<i; j++) {
		statement; // 
	}
}

// O(n2) Time
```

```C++
int p = 0
for(int i=1; p<=n; i++) {
	p += i; 
}

// O(sqrt(n)) Time
```

```C++
for(int i=1; i<n; i *= 2) {
	statement; // n Time
}

// O(n) Time
```

---
## Links

- [[Time Complexity]]
- [[Big O Notation]]
- [[Frequency Count Method]]

---

## Source

- 