202402090316
# Other Conditionals Analyzation

## Notes

While loop terminating conditional can vary from simple to complex hence determining the Time/Space Complexity of such is a bit more involved

```C++
int i = 0;

while(i<n){
	statement;
	i++;
}
```
The above while loop is basically identical to a typical for loop which derives a time complexity of O(n)
```C++
int a = 1;

while(a < b){
	statement;
	a *= 2;
}
```
Since the incrementing value is exponential (2$^k$) it will reach the terminating value $b$ in O(log(n)) time

Most while loops will have a similar if not identical terminating conditional as a for loop. Even though the structure is different the steps taken will be the same and therefore have the same time complexity

```C++
int gcd(int m, int n) {
	while(m != n) {
		if(m > n) {
			m -= n;
		} else {
			n -= m;
		}
	}
}
```
A more complex example but breaking it down the conditional in terms of n will run about n/m time which reduces to just O(n)
```C++
void test(n) {
	if(n < 5){
		printf("%d", n);
	} else {
		for(int i=0; i<n; i++) {
			printf("%d", i);
		}
	}
}
```
For branching conditionals if there are 2 or more branches the time complexity will have a best and worst case scenario. In this particular example the best case is in the if branch (a single statement so O(1) time) but the else branch would produce the worst case (a standard for loop O(n) time). In the case of having only 1 branching conditional the time complexity would be for the single branch only.


---
## Links

- [[How to Analyze an Algorithm]]
- [[Algorithm]]

---

## Source

- 