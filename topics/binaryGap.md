
# Binary Gap

## Problem statement

A binary gap within a positive integer N is any maximal sequence of consecutive zeros that is surrounded by ones at both ends in the binary representation of N.

For example, number 9 has binary representation 1001 and contains a binary gap of length 2. The number 529 has binary representation 1000010001 and contains two binary gaps: one of length 4 and one of length 3. The number 20 has binary representation 10100 and contains one binary gap of length 1. The number 15 has binary representation 1111 and has no binary gaps. The number 32 has binary representation 100000 and has no binary gaps.

Write a function:

class Solution { public int solution(int N); }

that, given a positive integer N, returns the length of its longest binary gap. The function should return 0 if N doesn't contain a binary gap.

For example, given N = 1041 the function should return 5, because N has binary representation 10000010001 and so its longest binary gap is of length 5. Given N = 32 the function should return 0, because N has binary representation '100000' and thus no binary gaps.

Write an efficient algorithm for the following assumptions:

N is an integer within the range [1..2,147,483,647].


## Number System Classification

* Base 10 (Decimal) — Represent any number using 10 digits [0–9]
* Base 2 (Binary) — Represent any number using 2 digits [0–1]
* Base 8 (Octal) — Represent any number using 8 digits [0–7]
* Base 16(Hexadecimal) — Represent any number using 10 digits and 6 characters [0–9, A, B, C, D, E, F]

Reference : https://www.cuemath.com/numbers/number-systems/

### Binary 

Represented in 1's or 0's  
    
    * 32 bit and range of unsigned integer is 2^0 to 2^31 -1 (double Mersenne)
    * 64 bit and range unsigned integer is 2^0 to 2^64 -1
    
## Format

* 100101 binary (explicit statement of format)
* 100101b (a suffix indicating binary format; also known as Intel convention)
* 0b100101 (a prefix indicating binary format, common in programming languages)
* 6b100101 (a prefix indicating number of bits in binary format, common in programming languages)
* '#b100101' (a prefix indicating binary format, common in Lisp programming languages) 


#### Decimal to Binary

Given number is 17 

```
    2|17  1
     |____
    2|8   0
     |____
    2|4   0
     |____
    2| 2  0
     |____
       1
       
     Binary number is 10001

```
     
### Binary to Decimal 

Formula: 

For binary number with n digits:

dn-1 ... d3 d2 d1 d0

The decimal number is equal to the sum of binary digits (dn) times their power of 2 (2<sup>n</sup>):

```
17  - 10001
    - (1 X 2pow4) + (0 X 2pow3) + (0 X 2pow2) + (0 X 2pow1)  + (1 X 2pow0)
    - 16 + 0 + 0 + 0 + 1
    - 17
```

## Solutions

#### Approach 1 - While loop

Time Complexity : O(LogN)
Space Complexity : O(1)
```
def solution_1(N):
    max_gap,current_gap = 0,0

    while N > 0 and N % 2 == 0:
        N //= 2

    while N > 0:
        remainder = N % 2
        if remainder == 0:
            current_gap += 1
        else:
            if current_gap != 0:
                if current_gap > max_gap:
                    max_gap = current_gap
                current_gap = 0
        N //= 2

n = 529;
solution_3(n);
```

#### Approach2 - Right wise Binary

   “x” with an integer “y” denoted as '(x>>y)' is equivalent to dividing x with 2^y.
   
   * 17 -> 10001
   * 17 >> 1 => 01000 (8)

Time Complexity : O(LogN)
Space Complexity : O(1)
```
def solution_2(n):
    # Size of an integer is
    # assumed to be 32 bits
    counter, maxCounter = 0, 0

    for i in range(n.bit_length() -1, -1, -1):
        k = n >> i;
        if (k & 1):
            print("1", end="");
            maxCounter = max(counter, maxCounter)
            counter = 0
        else:
            print("0", end="");
            counter += 1

    print('max Counter')
    print(maxCounter)

n = 529;
solution_2(n);

```

### Approach3 - Using In build Functions 

Time Complexity : 0(logn) + O(n)
Space Complexity : O(1)

```

def solution_3(N):
    # Convert to Binary 
    number = bin(N)[2:]
    counter, maxCounter = 0, 0
    
    # Iterate the binary digits and count the number
    for i in number:
        if int(i) == 0:
            counter += 1
        elif int(i) == 1:
            maxCounter = max(counter, maxCounter)
            counter = 0
    return maxCounter

print(solution_3(2147483647))
```

## Similar problems

    * Same question can be rewritten to check adjacent 1's instead of 0.
        Ref : https://leetcode.com/problems/binary-gap/ 