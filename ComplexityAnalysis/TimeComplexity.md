# What is Time complexity?

A measure of how fast

*For Example we have an Array*

a = [1,2,3,4,5,6,7]

- If we need 1 from Array it's available in a[0] - Best Case
- If we need 4 from Array it's available in a[3] - Medium Case
- If we need 7 from Array it's available in a[6] - Worst Case -> Big O (Alaways choosen)

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


## Complexities Notation:

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
