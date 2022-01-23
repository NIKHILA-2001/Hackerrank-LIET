# String Diagonals
Write a program that takes a string as input and prints it in the following manner :
Ex : if the string is "hello", output should be
```
H   o
 e l
  l
 e l
h   o
```
**Sample Input 0**
```
hello
```
**Sample Output 0**
```
h   o
 e l
  l
 e l
h   o
```
### Solution(C):

```c
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
int main()
{
	char s[100];
    int n;
    scanf("%s",s);
    n=strlen(s);
    for(int i=0;i<n;i++){
        for(int j=0;j<n;j++)
            if(j==i||j==(n-i-1))
               printf("%c",s[j]); 
            else
                printf(" ");
        printf("\n");
    }
	return 0;
}
```
