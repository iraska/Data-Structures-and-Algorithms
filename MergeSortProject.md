# Project 2: Merge Sort Project
**[16,21,11,8,12,22] ->** *Merge Sort*

## 1. Write the stages of the above array according to the sort type.
*The main purpose of Merge Sort is to divide the number sequence until only one cell remains, and then combine the numbers to form an ordered sequence.*

**1.** First, we split the array in half.

- [16,21,11] [8,12,22]

**2.** We continue to divide the resulting new sequences in half until only one cell remains.

- [16,21,11] --> [16,21] [11] --> [16] [21] and [11]
- [8,12,22] --> [8,12] [22] --> [8] [12] and [22]

**3.** Then we move on to the merge phase, and we sort from smallest to largest when combining.

- [16,21] and [11] --> [11,16,21]
- [8,12] and [22] --> [8,12,22]

**4.** In the last step, we combine the small ordered sequences to obtain our new ordered sequence.

- **[8,11,12,16,21,22]**

## 2. Write the Big-O notation.

- Since we are evaluating on an element basis, the Time Complexity is o(n) and the number of scanned elements does not change.
- This is done:
 2^x = n --> x = ***logn*** times since it is halved each time (It's actually log2n times, but it's the character that matters).
 - It was coming o(n) times in each transaction, then if we evaluate all cases, our Time Complexity is **o(nlogn)**.

*Big-o notation =* **0(nlogn)**
