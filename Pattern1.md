PRINT THE BELOW MENTIONED PATTERN FOR ANY "N" VALUE. WHERE "N" INDICATES NO.OF ROWS.

Input Format

A SINGLE INTEGER DENOTING N VALUE

Constraints

1<=N<=100

Output Format

PATTERN AS SHOWN IN SAMPLE TEST CASE

Sample Input 0<br/>
`
5
` <br/>
Sample Output 0
```
    1
   12
  123
 1234
12345
```
### Solution
```py
s=''
n=int(input())
for i in range(1,n+1):
    s=s+str(i)
    print(s.rjust(n))
```
