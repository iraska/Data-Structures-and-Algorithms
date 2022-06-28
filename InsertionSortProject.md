# Project 1: Insertion Sort Project
**[22,27,16,2,18,6] ->** *Insertion Sort*
## 1. Write the stages of the above given sequence according to the sort type.
- Starting from the first number, the smallest element of the number block is found.  

[22,27,16,**2**,18,6]

- The number found is written first and the place of the first number and the number found (smallest number) is replaced.  

[**2**,27,16,**22**,18,6]

- At the moment the first number is the smallest number. We now expect the second number to be the smallest number. The new smallest number is determined and replaced with the second element.  

[*2*,**6**,16,22,18,**27**]

- The same operations are applied for the other elements, respectively.

[2,6*,**16**,22,18,27]  
[*2,6,16*,**18**,**22**,27]  
[*2,6,16,18,22*,**27**]

- The ordered array we get is as follows:

**[2,6,16,18,22,27]**

## 2. Write the Big-O notation.
*Big-o notation gives us the functional characteristic structure between input and output.*  
*It looks at what can be generalized according to n input size.*  

1. Assuming there are n values; In the first step, we checked ***n*** of them while finding the smallest element.  
2. In the second stage, we performed ***n-1*** transactions.
3. So, if we look at the algorithm roughly: n + (n-1) + (n-2) + ... + 1 = the sum of the numbers from 1 to n.

n*(n+1)/2 = (***n^2*** + n)/2 --> *Big-o notation is based on the dominant factor.*

Big-o notation = **o(n^2)**

## 3. What case does the number 18 fall into after the array is sorted? Write.
*Time Complexity:* 
- ***Average case:*** *The number we are looking for is in the middle,* 
- ***Worst case:*** *The number we are looking for is at the end,* 
- ***Best case:*** *The number we are looking for is at the beginning of the series.*

[2,6,16,**18**,22,27] --> Included in the **Average case**.

## 4. Write the first 4 steps of [7,3,5,8,2,9,4,15.6] according to Insertion Sort.
1. [7,3,5,8,**2**,9,4,15.6] --> [**2**,3,5,8,**7**,9,4,15.6]
2. [*2*,**3**,5,8,7,9,4,15.6]
3. [*2,3*,5,8,7,9,**4**,15.6] --> [2,3,**4**,8,7,9,**5**,15.6]
4. [*2,3,4*,8,7,9,**5**,15.6] --> [*2,3,4*,**5**,7,9,**8**,15.6]
