202402020336
# Frequency Count Method

## Notes

Measures the time it takes for an algorithm to run

Example Analysis:
``` C++
int sum(arr, n) {
	// arr is n SU(Space Unit ie Word) n is 1 SU(Word)
	s = 0; // 1 TU(Time Unit) 1 SU
	for(int i=0; i < n; i++){ // n + 1 TU i is 1 SU(Word)
	//(1 TU; len+1 TU; len TU): take largest TU from for loop (conditional)
		s += arr[i]; // len TU
	}
	return s; // 1 TU
}
```

Time function (sum of all TU) f(n) = 2n + 3
O(n) time since the degree of the polynomial above is 1

Space function (sum of all SU) s(n) = n + 3
O(n) space since the degree of the polynomial above is 1

Degree is measured by the largest magnitude of exponents of a variable (this is n to the 1 power in space and time complexity)


---
## Links

- [[Algorithm]]
- [[How to Analyze an Algorithm]]
- [[Big O Notation]]
- [[Time Complexity]]
- [[Space Complexity]]

---

## Source

- 