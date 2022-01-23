# Sum of Consecutive Primes
A positive integer may be expressed as a sum of different prime numbers (primes), in one way or another.
Given two positive integers n and k, you should count the number of ways to express n as a sum of k different primes.
Here, two ways are considered to be the same if they sum up the same set of the primes.
For example, 8 can be expressed as 3 + 5 and 5 + 3 but they are not distinguished.
When n and k are 24 and 3 respectively, the answer is two because there are two sets {2, 3, 19} and {2, 5, 17} whose sums are equal to 24.
There are no other sets of three primes that sum up to 24.
For n = 24 and k = 2, the answer is three, because there are three sets {5, 19}, {7, 17} and {11, 13}.
For n = 2 and k = 1, the answer is one, because there is only one set {2} whose sum is 2.
For n = 1 and k = 1, the answer is zero. As 1 is not a prime, you shouldn’t count {1}.
For n = 4 and k = 2, the answer is zero, because there are no sets of two different primes whose sums are 4.
Output the number of such ways for the given n and k.

**Input Format**

The input is a sequence of datasets followed by a line containing two zeros separated by a space.
A dataset is a line containing two positive integers n and k separated by a space.

**Constraints**

n ≤ 1120 and k ≤ 14.

**Output Format**

The output should be composed of lines, each corresponding to an input dataset.
An output line should contain one non-negative integer indicating the number of ways for n and k specified in the corresponding dataset.
You may assume that it is less than 2^31.

### Solution(Python):
```py
int ans[1125][15]= {0};
int main()
{
    int n, k, prim[1000], i, x = 0, len = 187, j;
    int d[] = {2,3,5,7,11,13,17,19,23,29,31,37,41,43,47,53,59,61,67,71,73,79,83,89,97,101,103,107,
               109,113,127,131,137,139,149,151,157,163,167,173,179,181,191,193,197,199,211,223,227,229,
               233,239,241,251,257,263,269,271,277,281,283,293,307,311,313,317,331,337,347,349,353,
               359,367,373,379,383,389,397,401,409,419,421,431,433,439,443,449,457,461,463,467,
               479,487,491,499,503,509,521,523,541,547,557,563,569,571,577,587,593,599,601,607,
               613,617,619,631,641,643,647,653,659,661,673,677,683,691,701,709,719,727,733,739,
               743,751,757,761,769,773,787,797,809,811,821,823,827,829,839,853,857,859,863,877,
               881,883,887,907,911,919,929,937,941,947,953,967,971,977,983,991,997,1009,1013,
               1019,1021,1031,1033,1039,1049,1051,1061,1063,1069,1087,1091,1093,1097,1103,1109,1117};
    ans[0][0] = 1;
    for(i = 0; i < len; ++i)
        for (j = 1120 - d[i]; j >= 0; --j)
            for(k = 1; k <= 14; ++k)
                ans[j + d[i]][k] += ans[j][k - 1];
    while (scanf("%d%d", &n, &k) == 2 && (n || k))
        printf("%d\n", ans[n][k]);
    return 0;
}
```
