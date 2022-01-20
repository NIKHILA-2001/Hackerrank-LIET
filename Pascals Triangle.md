# Pascal's Triangle
Pascal's Triangle in Mathematics is the following pattern :
```
1
1 1
1 2 1
1 3 3 1
and so on
```
For Cth element in row R, it is equal to the sum of elements C and C-1 in row R-1.
The first and the last elements of every row are always 1.

Your task is given a number K, print the first K rows of the pascals triangle.

**Input Format**

Only one integer, the value of K.

**Constraints**

1 <= K <= 50

**Output Format**

Output K lines, the first K rows of the pascal's triangle.

Sample Input 0
```
4
```
Sample Output 0
```
1
1 1
1 2 1
1 3 3 1
```
### Solution( Python ):

```py
n=int(input())
for i in range(1,n+1):
    C=1
    for j in range(1,i+1):
        print(C,end=' ')
        C=int(C*(i-j)/j)
    print()
```
