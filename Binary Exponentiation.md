# Binary Exponentiation

Write a program to print the value of (AB) % M, given the values of A, B and M.
Remember, those who use an O(B) function to find the value of AB are scum. But those who use the inbuilt library function to find the value of AB and then do %M are worse than scum.

**Input Format**

Three integers, A, B and M.

**Constraints**

1 <= A, B, M <= 1012

**Output Format**

Output one integer denoting the value of AB % M.

**Sample Input 0**
```
2 3 3
```
**Sample Output 0**
```
2
```
### Solution(Python):

```py
def quad_pow(base, exponent, modul): 
    alpha = (bin(exponent).replace('0b', ''))[::-1]
    a = 1
    b = base
    for i in range(0, len(alpha)):
        if int(alpha[i]) == 1:
            a = (a * b) % modul
        b = (b*b) % modul
    return a
a,b,c = input().split()
a,b,c = int(a), int(b), int(c)
print(quad_pow(a,b,c))
```
