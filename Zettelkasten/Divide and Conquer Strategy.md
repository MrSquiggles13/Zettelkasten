202402220507
# Divide and Conquer Strategy

## Notes

The application of taking a large problem and breaking it down into smaller more manageable problems. Those sub-problems can be broken down even more if necessary. It is essential that each sub-problem be the same type of problem as the main problem i.e. if the main problem is to sort then the sub-problems should also be to sort. Each sub-problem should have its own solution that can be combined with all other sub-problems' solutions to generate an adequate main solution for the main problem.

![[Pasted image 20240223052757.png]]

In this diagram there is a main problem, P, that is of size n. P is then broken down into sub-problems $P_1$ to $P_k$. Each one of these sub-problems has a solution, $S_1$ to $S_k$ which can be combined into a main solution, S.


This is  the divide and conquer strategy in algorithmic format:
```C
Algo DAC(P){
	if(small(P)){
		S(P);
	} else {
		divide P into P1, P2 ... Pk
		Apply DAC(P1), DAC(P2) ... DAC(Pk)
		Combine(DAC(P1), DAC(P2) ... DAC(Pk)) 
	}
}
```

The problem (P) is an input for divide and conquer algorithm (DAC()). If the problem input (P) is a sub-problem of the main problem (small(P)) then solve the problem (S(P)). Else then divide the problem (P) into sub-problems (P1, P2 ... Pk) and use it as input for another divide and conquer algorithm call (DAC(P1), DAC(P2) ... DAC(Pk)). Then use the output from those calls and combine them together, which will be solutions to the problems from the terminating condition in the recursive function (Combine(DAC(P1), DAC(P2) ... DAC(Pk))) which will be the main solution to the main problem.

---
## Links

- [[Problem Solving Strategy]]
- [[Algorithm]]

---

## Source

- [Bari's Algorithm Playlist 2](https://youtu.be/2Rr2tW9zvRg?si=SD_TKCuE0YoFNBPl)