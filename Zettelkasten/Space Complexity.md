202402070118
# Space Complexity

## Notes


Measured through a unit of space which is also referred to as a Word.  This determines the max possible memory an algorithm will utilize.

Example Space:
```C++
int addMatrices(A, B, n) { // A and B is n2 Words n is 1 Word
	for(int i=0; i<n; i++) { // i is 1 Word
		for(int j=0; j<n; j++){ // j is 1 word
			C[i,j] = A[i,j] + B[i,j]; // C is n2 Words
		}
	}
}
```

Total summation polynomial above is: s(n) = 3n$^2$ + 3
The space complexity is O(n$^2$) since n$^2$ is the highest degree in the polynomial above

---
## Links

- [[Big O Notation]]
- [[Frequency Count Method]]

---

## Source

- 