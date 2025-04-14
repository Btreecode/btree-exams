0. n / 2  
1. (n + 1) / 2  
0. n  
0. n - 1  
0. (n - 1) / 2  

Consider the following loop, where n is some positive integer:

```java
for (int i = 0; i < n; i += 2)
{
    if (/* test */)
    {
        /* perform some action */
    }
}
```
In terms of n, which Java expression represents the maximum number of times that
/* perform some action */ could be executed?

---

0. 9  
0. 11  
0. 13  
1. 20  
0. 33  

Consider the following code segment.

```java
int[][] mat = {{3, 4, 5},
               {6, 7, 8}};

int sum = 0;
for (int[] arr : mat) {
    for (int n = 0; n < mat.length; n++) {
        sum += arr[n];
    }
}
```

---