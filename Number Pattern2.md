# NUMBER PATTERN

PRINT THE BELOW MENTIONED PATTERN FOR ANY "N" VALUE. WHERE "N" INDICATES NO.OF ROWS.

**Input Format**

A SINGLE INTEGER DENOTING N VALUE

**Constraints**

1<=N<=100

N is only odd

**Output Format**

PATTERN AS SHOWN IN SAMPLE TEST CASE

**Sample Input 0**
```
5
```
**Sample Output 0**
```
1   5
 2 4
  3
```
### Solution (Python):
```py
s=''
n=int(input())
for i in range(1,int((n+1)/2)+1):
    for j in range(1,n+1):
        if(i==j):print(i,end="")
        elif(j==n-i+1): print(j,end="")
        else: print(" ",end="")
    print()
```
