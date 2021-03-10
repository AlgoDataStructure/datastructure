
## What is Log?

In Maths log means log<sub>10</sub>, in Computer science log<sub>2</sub>.


log<sub>2</sub> 16 = ?
2^4 = 16

log<sub>2</sub> 16 = 4;

log<sub>2</sub> 8 = ?

2^3 = 8
log<sub>2</sub> 8 = 3;

log<sub>2</sub> 12 =?

2^3 = 8
2^4 = 16
log<sub>2</sub> 12 = 3.5


# What is Time complexity?

Time complexity of an algorithm quantifies the amount of time taken by an algorithm to solve the computational problem.

*For Example we have an Array*

a = [1,2,3,4,5,6,7]

- If we need 1 from Array it's available in a[0] - Best Case
- If we need 4 from Array it's available in a[3] - Medium Case
- If we need 7 from Array it's available in a[6] - Worst Case -> Big O (Alaways choosen)


## Linear Time 

0(n) where n is the number of input , if the size of the array or input increases then the execution time also increases. Commom example, increasing the size of array length

```
n= 100000
for(i=0;i<n;i++){
    console.log(i);
}
```

## Constant Time 

0(n) where n is the number of input , if the size of the array or input increases then the execution time remains same . 

```
n= 5
for(i=0;i<n;i++){
    console.log(i);
}
```

Say for example for the above program it takes 0.2 seconds for the input 5 and the same time will be taken for the input 30.

## Logarithmic Time 

### 0(nlogn)  

n=8  

log 2^n  where n=3

Use Case 

- Merge Sort 
- Quick Sort.

```
1. [1,4,5,6,7,8,3,5.6]

2. [1,4,5,6]  [8,3,5,6]

3.  [1,4] [5,,6]  [8,3] [5,6]

base level  [1] [4] [5] [6] [8] [3] [5] [6]

```
### 0(n^2)  

- Bubble Sort
- Insertion Sort
- Selection Sort

Take the first element and comparing with other element.

```
1. [8,3,5.6]

    compare 8 with 3,5,6
	compare 3 with 8,5,6
	compare 5 with 8.3,6
	compare 6 with 8,3,5
	
```

### 0(2^n) - Exponential Time

- Recursion
- BackTracking Algorithm


###  0(n!) - Factorial Time

- Permutation 
- Factorial 
