# What is Complexity Analysis? Why it's needed?

The process of determining how efficient the algorithm is. Complexity analysis involves both Time and Space Complexities of an Algorithm.

It's needed to determine the better algorithm for the purpose.

It is classified into 3 types.

1. Best Case - Big Omega
2. Medium Case - Big Theta
3. Worst Case - Big O

## Complexities Representation:

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

