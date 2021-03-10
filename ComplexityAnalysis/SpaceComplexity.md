# Space complexity

Space complexity of an algorithm quantifies the amount of space or memory taken by an algorithm to solve the computational problem.


## Fixed part  - Independant
```
	sum(a,b)
		return a+b
	
	a and b is fixed part where it requires 4 bytes per variable
```

## Variable part   - Dependant

```
	sum(x,n)
		total =0 
		for(i=0: i <n; i++) {
			total = total + x[i]
		}
	
	total, x and n are variables suppose n is large and we need to store 100 units.
	
```

## Auxillary Space 

It is the temporary space allocated by your algorithm to solve the problem.

Space complexity = Input Size + Auxillary Space.

```
	sum(a,b)
		return a+b
	
	a and b is fixed part where it requires 4 bytes per variable
	a+b will be used in Auxillary space
```

## To design the algorithm
 
Time complexity much be lower, where the space complexity can be higher.

Fibonacci 

							5
					3      			2
			2			1			0		1	
		1		1  