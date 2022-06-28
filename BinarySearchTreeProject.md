# Project 3: Binary Search Tree Project
## Write the Binary-Search-Tree stages of the sequence [7, 5, 1, 8, 3, 6, 0, 9, 4, 2].
**1.** We keep the Binary Search Tree as references to two sides (right and left).

**2.** First we will select a root and we will have elements greater than root on the right and elements less than root on the left.

   - ***Example:*** *root is x. y is found to the right of root. To its left is a z, etc.*

Binary Search Tree of **[7, 5, 1, 8, 3, 6, 0, 9, 4, 2]**:

* Let's have root = 6
1) 7 is located to the right of root.

|   |   |6   |   |   |
|---|---|---|---|---|
|   |   |   | \  |   |
|   |   |   |   |  7 |

2) 5 is located to the left of root.

|   |   | 6  |   |   |
|---|---|---|---|---|
|   | /  |   | \  |   |
| 5  |   |   |   |  7 |

3) 1 is located to the left of root. It is also to the left of 5.

|   |   |   |   | 6  |   |   |
|---|---|---|---|---|---|---|
|   |   |   | /  |   | \  |   |
|   |   | 5  |   |   |   |  7 |
|   | /  |   |   |   |   |   |
| 1  |   |   |   |   |   |   |

4) 8 is located to the right of root. It is also to the right of 7.

|   |   |   |   |  6 |   |   |   |   |
|---|---|---|---|---|---|---|---|---|
|   |   |   | /  |   | \  |   |   |   |
|   |   | 5  |   |   |   | 7  |   |   |
|   | /  |   |   |   |   |   |  \ |   |
| 1  |   |   |   |   |   |   |   | 8  |

5) 3 is located to the left of root. It is also to the left of 5 but to the right of 1.

|   |   |   |   |  6 |   |   |   |   |
|---|---|---|---|---|---|---|---|---|
|   |   |   | /  |   |  \ |   |   |   |
|   |   |  5 |   |   |   | 7  |   |   |
|   | 1  |   |   |   |   |   | \  |   |
|   |   |  \ |   |   |   |   |   |  8 |
|   |   |   | 3  |   |   |   |   |   |

6) 0 is located to the left of root. It is also to the left of 5 and 1.

|   |   |   |   |   |   |  6 |   |   |   |   |
|---|---|---|---|---|---|---|---|---|---|---|
|   |   |   |   |   | /  |   |  \ |   |   |   |
|   |   |   |   |  5 |   |   |   | 7  |   |   |
|   |   |   | /  |   |   |   |   |   | \  |   |
|   |   |  1 |   |   |   |   |   |   |   |  8 |
|   |  / |   | \  |   |   |   |   |   |   |   |
| 0  |   |   |   |  3 |   |   |   |   |   |   |

7) 9 is located to the right of root. It is also to the right of 7 and 8.

|   |   |   |   |   |   |  6 |   |   |   |   |   |   |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|   |   |   |   |   | /  |   |  \ |   |   |   |   |   |
|   |   |   |   |  5 |   |   |   |  7 |   |   |   |   |
|   |   |   | /  |   |   |   |   |   | \  |   |   |   |
|   |   |  1 |   |   |   |   |   |   |   | 8  |   |   |
|   | /  |   |  \ |   |   |   |   |   |   |   | \  |   |
|  0 |   |   |   |  3 |   |   |   |   |   |   |   |  9 |

8) 4 is located to the left of root. It is also to the left of 5 but to the right of 1 and 3.

|   |   |   |   |   |   | 6  |   |   |   |   |   |   |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|   |   |   |   |   | /  |   |  \ |   |   |   |   |   |
|   |   |   |   |  5 |   |   |   | 7  |   |   |   |   |
|   |   |   | /  |   |   |   |   |   | \ |   |   |   |
|   |   | 1  |   |   |   |   |   |   |   | 8  |   |   |
|   | /  |   |  \ |   |   |   |   |   |   |   |  \ |   |
| 0  |   |   |   |  3 |   |   |   |   |   |   |   | 9  |
|   |   |   |   |   |  \ |   |   |   |   |   |   |   |
|   |   |   |   |   |   | 4  |   |   |   |   |   |   |

9) 2 is located to the left of root. It is also to the left of 5 but to the right of 1. However it should be located to the left of 3.


|   |   |   |   |   |   | 6  |   |   |   |   |   |   |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|   |   |   |   |   | /  |   |  \ |   |   |   |   |   |
|   |   |   |   |  5 |   |   |   | 7  |   |   |   |   |
|   |   |   | /  |   |   |   |   |   | \ |   |   |   |
|   |   | 1  |   |   |   |   |   |   |   | 8  |   |   |
|   | /  |   |  \ |   |   |   |   |   |   |   |  \ |   |
| 0  |   |   |   |  3 |   |   |   |   |   |   |   | 9  |
|   |   |   |  / |   |  \ |   |   |   |   |   |   |   |
|   |   | 2  |   |   |   | 4  |   |   |   |   |   |   |
