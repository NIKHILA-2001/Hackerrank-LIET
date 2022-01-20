# TRIANGLE QUEST

You are given a positive integer N. Print a numerical triangle of height N-1.

**Input Format**
A single line containing integer, N.

**Constraints**
1<=N<=9

**Output Format**
Print N-1 lines as explained below.

## (1)
**Sample Input**
```
5
```
**Sample Output**
```
1
22
333
4444
```
### Solution(Python):
```py
for i in range(1,int(input())): #More than 2 lines will result in 0 score. Do not leave a blank line also
    print((10**i)//9*i)
```

## (2)
**Output Format**
Print N lines as explained below.

**Sample Input**
```
5
```
**Sample Output**
```
1
121
12321
1234321
123454321
```
### Solution(Python):
```py
for i in range(1,int(input())+1): #More than 2 lines will result in 0 score. Do not leave a blank line also
    print(int(10**i/9)**2)
```
