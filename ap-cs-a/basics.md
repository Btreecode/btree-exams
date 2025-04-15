1. a[i] == max  
0. a[i] != max  
0. a[i] < max || a[i] > max  
0. true  
0. false  

The boolean expression `a[i] == max || !(max != a[i])` can be simplified to:

---

0. (1) n == 1 && n == 4   (2) k = n  
0. (1) n == 1 && n == 4   (2) k += 4  
0. (1) n == 1 || n == 4   (2) k += 4  
1. (1) n == 1 || n == 4   (2) k += n  
0. (1) n == 1 || n == 4   (2) k = n - k  

Consider the code segment:

```java
if (n == 1)
  k++;
else if (n == 4)
  k = 4;
```
Suppose that the given segment is rewritten in the form:
```java
if (/* condition */)
  /* assignment statement */;
```
Given that `n` and `k` are integers and that the rewritten code performs the same task as the original code,
which of the following could be used as (1) condition and (2) assignment statement?

---

0. arrays a and b contain identical elements in the same order.  
0. arrays a and b contain identical elements in reverse order.  
0. arrays a and b are permutations of each other.  
0. array a contains at least one element that is also in b.  
1. every element of array a is also in b.  

Consider method `findSomething` below.

```java
/** Precondition: a.length is equal to b.length. */
public static boolean findSomething(int[] a, int[] b)
{
    for (int aValue : a)
    {
        boolean found = false;
        for (int bValue : b)
        {
            if (bValue == aValue)
                found = true;
        }
        if (!found)
            return false;
    }
    return true;
}
```
Which best describes what method `findSomething` does?
Method `findSomething` returns `true` only if

---

