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

1. 3 4 5  
0. 4 5 6  
0. 5 6 7  
0. 0 0 0  
0. No output will be produced. An ArrayIndexOutOfBoundsException will be thrown.  

What output will be produced by invoking `firstTestMethod` for a `Tester` object?

```java
public class Tester
{
    private int[] testArray;

    public Tester()
    {
        testArray = new int[3];
        testArray[0] = 3;
        testArray[1] = 4;
        testArray[2] = 5;
    }

    /** @param n an int to be incremented by 1 */
    public void increment(int n)
    {
        n++;
    }

    public void firstTestMethod()
    {
        for (int i = 0; i < testArray.length; i++)
        {
            increment(testArray[i]);
            System.out.print(testArray[i] + " ");
        }
    }

    public void secondTestMethod()
    {
        for (int element : testArray)
        {
            increment(element);
            System.out.print(element + " ");
        }
    }
}
```

---

1. 3 4 5  
0. 4 5 6  
0. 5 6 7  
0. 0 0 0  
0. No output will be produced. An ArrayIndexOutOfBoundsException will be thrown.  

What output will be produced by invoking `secondTestMethod` for a `Tester` object, assuming that `testArray` contains 3, 4, 5?

```java
public class Tester
{
    private int[] testArray;

    public Tester()
    {
        testArray = new int[3];
        testArray[0] = 3;
        testArray[1] = 4;
        testArray[2] = 5;
    }

    /** @param n an int to be incremented by 1 */
    public void increment(int n)
    {
        n++;
    }

    public void firstTestMethod()
    {
        for (int i = 0; i < testArray.length; i++)
        {
            increment(testArray[i]);
            System.out.print(testArray[i] + " ");
        }
    }

    public void secondTestMethod()
    {
        for (int element : testArray)
        {
            increment(element);
            System.out.print(element + " ");
        }
    }
}
```

---

1. list[i] = (int) (Math.random() * 101);  
0. list.add((int) (Math.random() * 101));  
0. list[i] = (int) (Math.random() * 100);  
0. list.add(new Integer(Math.random() * 100));  
0. list[i] = (int) (Math.random() * 100) + 1;  

Consider the following `RandomList` class.

```java
public class RandomList
{
    private int[] ranList;

    public RandomList()
    { 
        ranList = getList(); 
    }

    /** @return array with random Integers from 0 to 100 inclusive */
    public int[] getList()
    {
        System.out.println("How many integers? ");
        int listLength = ...; // read user input
        int[] list = new int[listLength];
        for (int i = 0; i < listLength; i++)
        {
            /* code to add integer to list */
        }
        return list;
    }

    /** Print all elements of this list. */
    public void printList()
    {
        ...
    }
}
```
Which represents correct /* code to add integer to list */?

---

