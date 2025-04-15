0. I only  
0. II only  
0. III only  
0. I and III only  
1. II and III only  

Refer to the following method that finds the smallest value in an array:

```java
/** Precondition: arr is an array of nonzero length
  * and is initialized with int values.
  * @param arr the array to be processed
  * @return the smallest value in arr
  */
public static int findMin(int[] arr)
{
    int min = /* some value */;
    int index = 0;
    while (index < arr.length)
    {
        if (arr[index] < min)
            min = arr[index];
        index++;
    }
    return min;
}
```
Which replacement(s) for `/* some value */` will always result in correct execution of the findMin method?
```java
I.   Integer.MIN_VALUE  
II.  Integer.MAX_VALUE  
III. arr[0]
```

---

0. The method should be written on the assumption that there is only one value in the array that is larger than the given item.  
0. The method should be written so as to return the index of every occurrence of a larger value.  
1. The specification should be modified to indicate what should be done if there is more than one index of larger values.  
0. The method should be written to output a message if more than one larger value is found.  
0. The method should be written to delete all subsequent larger items after a suitable index is returned.  

A method is to be written to search an array for a value that is larger than a given item and return its index.  
The problem specification does not indicate what should be returned if there are several such values in the array.  
Which of the following actions would be best?

---

0. Removes from `list` the objects indexed at `i` and `j`  
0. Replaces in `list` the object indexed at `i` with the object indexed at `j`  
0. Replaces in `list` the object indexed at `j` with the object indexed at `i`  
0. Replaces in `list` the objects indexed at `i` and `j` with `temp`  
1. Interchanges in `list` the objects indexed at `i` and `j`  

Refer to the `doSomething` method below.

```java
// postcondition
public static void doSomething(ArrayList<SomeType> list, int i, int j)
{
    SomeType temp = list.get(i);
    list.set(i, list.get(j));
    list.set(j, temp);
}
```

Which best describes the postcondition for `doSomething`?

---

0. 3  
1. 4  
0. 5  
0. 10  
0. 13  

```java
public class Searcher
{
    private int[] arr;

    /** Constructor. Initializes arr with integers. */
    public Searcher()
    { /* implementation not shown */ }

    /**
     * Precondition: arr[first]...arr[last] sorted in ascending order.
     * Postcondition: Returns index of key in arr. If key not in arr,
     * returns -1.
     */
    public int search(int first, int last, int key)
    {
        int mid;
        while (first <= last)
        {
            mid = (first + last) / 2;
            if (arr[mid] == key) // found key, exit search
                return mid;
            else if (arr[mid] < key) // key to right of arr[mid]
                first = mid + 1;
            else // key to left of arr[mid]
                last = mid - 1;
        }
        return -1; // key not in list
    }
}
```

Consider the array `a` with values:
4, 7, 19, 25, 36, 37, 50, 100, 101, 205, 220, 271, 306, 321  

where 4 is `a[0]` and 321 is `a[13]`. Suppose that the `search` method is called with `first = 0` and `last = 13` to locate the key `205`.  

How many iterations of the `while` loop must be made in order to locate it?

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

0. Both implementations work as intended but Implementation 1 is faster than Implementation 2.  
0. Both implementations work as intended but Implementation 2 is faster than Implementation 1.  
0. Both implementations work as intended and are equally fast.  
1. Implementation 1 doesn't work as intended because the elements of prod are incorrectly assigned.  
0. Implementation 2 doesn’t work as intended because the elements of prod are incorrectly assigned.  

Consider a method `partialProd` that returns an integer array `prod` such that for all `k`, `prod[k]` is equal to  
`arr[0] * arr[1] * ... * arr[k]`. For example, if `arr` contains the values `{2, 5, 3, 4, 10}`,  
the array `prod` will contain the values `{2, 10, 30, 120, 1200}`.

```java
public static int[] partialProd(int[] arr) {
    int[] prod = new int[arr.length];
    for (int j = 0; j < arr.length; j++) {
        prod[j] = 1;
    }
    /* missing code */
    return prod;
}
```
Consider the following two implementations of /* missing code */.

**Implementation 1**
```java
for (int j = 1; j < arr.length; j++) {
    prod[j] = prod[j - 1] * arr[j];
}
```
**Implementation 2**
```java
for (int j = 0; j < arr.length; j++) {
    for (int k = 0; k <= j; k++) {
        prod[j] = prod[j] * arr[k];
    }
}
```
Which of the following statements is true?

---