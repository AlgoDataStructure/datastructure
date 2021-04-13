<div align="right">
    <b><a href="README.md">↥ back to Index</a></b>
</div>

Table of Contents
=================

   * [Time complexity](#time-complexity)
      * [Linear Time](#linear-time)
      * [Constant Time](#constant-time)
      * [Logarithmic Time](#logarithmic-time)
         * [0(nlogn)](#0nlogn)
         * [0(n^2)](#0n2)
         * [0(2^n) - Exponential Time](#02n---exponential-time)
         * [0(n!) - Factorial Time](#0n---factorial-time)
      * [Few more examples](#few-more-examples)
      
# Time complexity

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

## Few more examples

- `Big O(1):` Number of operation performed is 1 which is `sum`
```
a= 5
b= 10
sum = a+b
```

- `Big O(n):` Operation performed varies by `n` in this case print is operation and it depends on 'n'
```
n= 5
for(i=0;i<n;i++){
    console.log(i);
}
```
- `Big O(2n):` Number of operation performed varies by `n` in this case `print` is the operation in two blocks and it depends on 'n'
```
n= 5
for(i=0;i<n;i++){
    console.log(i);
}
for(i=0;i<n;i++){
    console.log(i);
}
```
- `Big O(n^2):` Number of operation performed varies by `n` in this case `print` is the operation in Nested blocks and it depends on 'n'
```
n= 5
for(i=0;i<n;i++){
  for(j=0;j<n;j++){
    console.log(i,j);
  }
}
```
- `Big O(log(n)):` 
Spliting the array until we reach single element in an array. Steps to spit,

  - Step 1: Split the array by 2
  - Step 2: Further split the Array[0] by 2
  - Step 3: Further split the Array[0][0] by 2
  - Step 4: Repeat untill you find the single element

  For array of lenght 3 the Log notation will be Log2 8 = 3

- `Big O(nlog(n))`: To perform single element for each element in an Array. Merge Sort: `nlog(n)`