202402070106
# Time Complexity

## Notes

Measured through theoretical units of time. Each statement in an algorithm is considered 1 unit of time and any kind of loop or sequential processing is compounded by the total possible times it could be ran.

Example Time:
```C++
int matrixMultiply(A, B, n) {
	for(int i=0; i<n; i++) { // n + 1 Time Unit
		for(int j=0; j<n; j++) { // n + 1 Time Unit * n Time Unit
			C[i, j] = 0; // n Time Unit * n Time Unit
			for(int k=0; k<n; k++) { // n + 1 Time Unit * n Time Unit * n Time Unit
				C[i, j] += A[i, k] * B[k, j]; // n Time Unit * n Time Unit * n Time Unit
			}
		}
	}
}
```

Total summation polynomial above is: f(n) = 2n$^3$ + 3n$^2$ + 2n + 1
The time complexity is O(n$^3$) since n$^3$ is the highest degree in the polynomial above

---
## Links

- [[Big O Notation]]
- [[Frequency Count Method]]
---

## Source

- [Bari's Algorithm Playlist 1.5.1](https://youtu.be/9TlHvipP5yA?si=90wIwXbzUl7JRKfL)