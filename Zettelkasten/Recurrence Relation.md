202402230558
# Recurrence Relation

## Notes

A method to find the time/space complexity of a recursive function

Given the recursive function:
```C
void Test(int n){
	if(n > 0){
		printf("%d", n);
		Test(n - 1);
	}
}
```

Do an analysis by using a tracing/recursive tree:
![[Pasted image 20240224021142.png]]

Here we can see that when Test is initially called with the integer 3 it will print out the current input which starts at three then continue to print out the previous input minus one until zero is reached in which the recursive function is no longer called.

Given that the function is called 4 times or input(3) plus one we can determine that with the input (n) the time complexity of the recursive function will be f(n) = n + 1 or O(n)

Analyze the function using substitution method:

```C
void Test(int n){ // --- T(n)
	if(n > 0){ // --- 1
		printf("%d", n); // --- 1
		Test(n - 1); // --- T(n-1)
	}
}
```

The function T(n) can be evaluated to $T(n)=T(n-1)+1$ since the call to itself can directly be placed in the equation alongside 1 which is a representative of constant time even though the conditional and the print statement would evaluate to 2 it just represents any value of constant time

$T(n)=\begin{cases} 1 & n=0 \\ T(n-1)+1 & n\gt0 \end{cases}$

This branching case evaluation shows the paths the recursive function could take when it is called as seen in the if conditional. This will help us to simplify and evaluate the function $T(n)=T(n-1)+1$ and find the time complexity

$T(n)=T(n-1)+1$
Evaluate T(n - 1)
$T(n-1)=T(n-2)+1$
Substitute T(n - 1)
$T(n)=[T(n-2)+1]+1$
$T(n)=T(n-2)+2$
Evaluate T(n - 2)
$T(n-2)=T(n-3)+1$
Substitute T(n - 2)
$T(n)=[T(n-3)+1]+2$
$T(n)=T(n-3)+3$
Since repeating replace constants with a variable (k)
$T(n)=T(n-k)+k$

Since the terminating branching case is when n == 0 we can assume that $n-k=0$
Evaluate
$n-k=0 == n=k$
Substitute
$T(n)=T(n-n)+n$
$T(n)=T(0)+n$
Since T(0) aka n=0 can be evaluated to a constant replace T(0) with that constant (1)
$T(n)=1 + n$

This shows the same conclusion as the tracing tree where the function is ran n+1 times or $T(n)=n+1$ OR $T(n)=\Theta(n)$

#### Other Examples

**_Function to evaluate_**
```C
void  Test(int n){ // --- T(n)
	if(n > 0){ // --- 1
		for(int i=0; i<n; i++){ // --- n + 1
			printf("%d", n); // --- n
		}
		Test(n-1); // --- T(n - 1)
	}
}
```

 We can derive from combining the time complexity of separate portions of the function that $T(n)=T(n-1)+2n+2$ which can be simplified to $T(n)=T(n-1)+n$ since if we only need the most significant value in its base term which would be n (any constants when able to be ignored). And we can derive the branching case evaluation from the function

$T(n)=\begin{cases} 1 & n=0 \\ T(n-1)+n & n\gt0 \end{cases}$

We can create a tracing tree with what we know of the function
![[Pasted image 20240224051454.png]]

This shows that a continuation will happen after T(n - 3) since it is repeating and will result to a constant that will eventually reduce to 0 and terminate the recursion. The left branch coming off of each function call representation is representative of how much time is taken inside the function itself i.e. n is the for loop and 2 is representative of T(2) called 2 times

When the calls are summated we get a series of incremental natural numbers i.e. 1, 2, 3, 4 ... etc. which can be replaced with the formula $\frac{n(n+1)}{2}$ which evaluated to asymptotic notation is $\Theta(n^2)$ 

Using the substitution method we can substitute and evaluate the function to see if we get the same result as the tracing tree

First is the function evaluation from the branching case n > 0
$T(n)=T(n-1)+n$
Substitute T(n-1) so function can be in terms of T(n)
$T(n-1)=T(n-2)+n-1$
$T(n)=[T(n-2)+n-1]+n$
We don't simplify here since the tracing tree showed we are looking for a series
$T(n)=T(n-2)+(n-1)+n$
Substitute T(n-2)
$T(n-2)=T(n-3)+n-2$
$T(n)=[T(n-3)+n-2]+(n-1)+n$
$T(n)=T(n-3)+(n-2)+(n-1)+n$
Since this seems to have an endless continuation we can replace the constants with a variable (k)
$T(n)=T(n-k)+(n-(k-1))+(n-(k-2))+...+(n-1)+n$
Now we can assume
$n-k=0$
Since the terminating value is when n=0 so we can solve for n
$n=k$
And now we can substitute k for n
$T(n)=T(n-n)+(n-n+1)+(n-n+2))+...+(n-1)+n$
Simplify
$T(n)=T(0)+1+2+...+(n-1)+n$
Which T(0) is already known to be 1 and the rest of the equation is the summation of natural numbers up to n which can be evaluated to $\frac{n(n+1)}{2}$ 
$T(n)=1+\frac{n(n+1)}{2}$
When written in asymptotic notation is $\Theta(n^2)$ which is the same answer we go with the tracing tree

**_Function to evaluate_**
```C
void Test(int n){ // --- T(n)
	if(n > 0){
		for(int i=1; i<n; i*=2){ 
			printf("%d", i); // --- log(n)
		}
		Test(n-1); // --- T(n-1)
	}
}
```

As before the time complexity of each statement is added together here it is $T(n)=T(n-1)+log(n)$ and derive the branching case evaluation

$T(n)=\begin{cases} 1 & n=0 \\ T(n-1)+log(n) & n\gt0 \end{cases}$

Tracing tree:
![[Pasted image 20240224065424.png]]

As above combine the time complexity of each function call
$log(n)+log(n-1)+log(n-2)+...+log(2)+log(1)$
Which can be refactored as
$log(n*(n-1)*(n-2)*...*2*1)$
In turn can be just
$log(n!)$

Now relating to how n! works with asymptotic notation it is known that n! is $O(n^n)$
Now when we plug that into or result replacing n!
$log(n^n)$
This equation can be derived as
$n(log(n))$ OR $O(n(log(n)))$

Using substitution method we can substitute and evaluate the function to see if we get the same result as the tracing tree

Write out the function to simplify
$T(n)=T(n-1)+log(n)$
Substitute T(n - 1)
$T(n-1)=T(n-2)+log(n-1)$
$T(n)=T(n-2)+log(n-1)+log(n)$
Substitute T(n - 2)
$T(n-2)=T(n-3)+log(n-2)$
$T(n)=T(n-3)+log(n-2)+log(n-1)+log(n)$
Repeating pattern calls for a continuation using variables for constants
$T(n)=T(n-k)+log(1)+log(2)+...+log(n-1)+log(n)$
Evaluate and simplify
$n-k=0$ SO $n=k$
Substitute k for n and reduce
$T(n)=T(0)+log(n!)$ OR $T(n)=1+log(n!)$
Which evaluates to
$T(n)=O(n(log(n)))$
And since that is the same answer as the tracing tree we can determine that is the right time complexity


**_Function to Evaluate_**
```C
void Test(int n){ // --- T(n)
	if(n > 0){
		printf("%d", n); // --- 1
		Test(n-1); // --- T(n - 1)
		Test(n-1); // --- T(n - 1)
	}
}
```

Summation of the time functions from each statement evaluates to
$T(n)=2T(n-1)+1$

Which gives us the branching cases
$T(n)=\begin{cases} 1 & n=0 \\ 2T(n-1)+1 & n\gt0 \end{cases}$

Tracing Tree:
![[Pasted image 20240225023842.png]]

A continuation is met after a repetition of the function and it is evaluated to take $2^k$ times to reach the terminating condition of T(0)

This can be written as $1+2+2^2+2^3+...+2^k$ which is a [[Geometric Progression]] that will equal to according to the formula $2^{k+1}-1$

Geometric progression formula:
$a+ar+ar^2+ar^3+...+ar^k=\frac{a(r^{k+1}-1)}{r-1}$
$a=1$ $r=2$ 
Substitute
$\frac{1(2^{k+1}-1)}{2-1}$
1 into $2^{k+1}-1$ is itself and 2 - 1 is 1 so also itself hence the result $2^{k+1}-1$
We can assume n-k = 0 hence n=k so we substitute
$T(n)=2^{n+1}-1$ 
And when defined in asymptotic notation
$T(n)=O(2^n)$

Using substitution method we can substitute and evaluate the function to see if we get the same result as the tracing tree

Function
$T(n)=2T(n-1)+1$
Evaluate and substitute for T(n-1)
$T(n-1)=2T(n-2)+1$
$T(n)=2[2T(n-2)+1]+1$
Simplify
$T(n)=2^2T(n-2)+2+1$
Evaluate and substitute for T(n-2)
$T(n-2)=2T(n-3)+1$
$T(n)=2^2[2T(n-3)+1]+2+1$
Simplify
$T(n)=2^3T(n-3)+2^2+2+1$
Continue for k times because of repetition
$T(n)=2^kT(n-k)+2^{k-1}+2^{k-2}+...+2^2+2+1$
Assume that n-k=0 so n=k and substitute
$T(n)=2^nT(0)+1+2+2^2+...+2^{k-1}$
Simplify
$T(n)=2^n*1+2^n-1$
$T(n)=2^n+2^n-1$
$T(n)=2^{n+1}-1$
Which in asymptotic notation would be
$T(n)=\Theta(2^n)$


---
## Links

- [[Recursion]]
- [[How to Analyze an Algorithm]]
- [[Geometric Progression]]

---

## Source

- [Bari's Algorithm Playlist 2.1.1](https://youtu.be/4V30R3I1vLI?si=FFm_ZqCZCwP5sBxI)
- [Bari's Algorithm Playlist 2.1.2](https://youtu.be/IawM82BQ4II?si=yViUHlHP-PZ1z0Tz)
- [Bari's Algorithm Playlist 2.1.3](https://youtu.be/MhT7XmxhaCE?si=P-T_u5u2lJGnOTz7)
- [Bari's Algorithm Playlist 2.1.4](https://youtu.be/JvcqtZk2mng?si=MrzL5VwJUsPMbCnx)