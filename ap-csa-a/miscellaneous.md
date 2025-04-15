0. ArrayIndexOutOfBoundsException  
0. IndexOutOfBoundsException  
0. NullPointerException  
1. ConcurrentModificationException  
0. ArithmeticException  

Consider the following code segment, which is intended to add zero to the end of `list` every time a certain condition is met. You may assume that `list` is an `ArrayList<Integer>` that contains at least one element.

```java
for (Integer num : list) {
    if (<condition>)
        list.add(0);
}
```

---

0. Only when x < y  
1. Only when x ≤ y  
0. Only when x > y  
0. For all values of x and y  
0. The method will never cause stack overflow  

When will method `whatIsIt` cause a stack overflow (i.e., cause computer memory to be exhausted)?

```java
public static int whatIsIt(int x, int y) {
  if (x > y)
    return x * y;
  else
    return whatIsIt(x - 1, y);
}
```
---

0. for (int i = 0; i <= list.size(); i++){  
 list.set(i, new Clown());  
}
1. list.add(list.size(), new Clown());
0. Clown c = list.get(list.size());
0. Clown c = list.remove(list.size());
0. list.add(-1, new Clown());

Consider a Clown class that has a no-argument constructor. Suppose a `list ArrayList<Clown> list` is initialized.
Which of the following will not cause an IndexOutOfBoundsException to be thrown?

---

0. 74  
0. 47  
0. 734  
0. 743  
1. 347  

```java
public static void whatsIt(int n) {
    if (n > 10)
        whatsIt(n / 10);
    System.out.print(n % 10);
}
```
What will be output as a result of the method call `whatsIt(347)`?

---

0. If the array is initially sorted in descending order, then insertion sort will be more efficient than selection sort.  
1. The number of comparisons for selection sort is independent of the initial arrangement of elements.  
0. The number of comparisons for insertion sort is independent of the initial arrangement of elements.  
0. The number of data movements in selection sort depends on the initial arrangement of elements.  
0. The number of data movements in insertion sort is independent of the initial arrangement of elements.  

A large list of numbers is to be sorted into ascending order.  
Assuming that a "data movement" is a swap or reassignment of an element, which of the following is a true statement?

---

1. Round-off error was caused by calculations with floating-point numbers  
0. Type boolean was not recognized by an obsolete version of Java  
0. An overflow error was caused by entering numbers that were too large.
0. c and d should have been cast to integers before testing for equality  
0. Bad test data were selected  

Three numbers a, b, and c are said to be a *Pythagorean Triple* if and only if the sum of the squares of two of the numbers equals the square of the third. A programmer writes a method `isPythTriple` to test if its three parameters form a Pythagorean Triple:

```java
// Returns true if a * a + b * b == c * c; otherwise returns false
public static boolean isPythTriple(double a, double b, double c) {
    double d = Math.sqrt(a * a + b * b);
    return d == c;
}
```
When the method was tested with known Pythagorean triples, isPythTriple sometimes erroneously returned false. What was the most likely cause of the error?

---


0. arr[first] < key < arr[last]  
0. arr[first] ≤ key ≤ arr[last]  
0. arr[first] < key < arr[last] or key is not in arr  
1. arr[first] ≤ key ≤ arr[last] or key is not in arr  
0. key ≤ arr[first] or key ≥ arr[last] or key is not in arr  

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
Which assertion is true just before each execution of the `while` loop?

---

0. The `Caller` object in the driver class was not created with `new`.  
0. The programmer forgot the `return` statement in `getList` that returns the list of `Integers`.  
0. The declaration of `numbers` is incorrect. It needed to be  
   `private ArrayList<Integer> numbers = null;`  
1. In the `getList` method, an attempt was made to add an `Integer` to an `ArrayList` that had not been created with `new`.  
0. The `shuffleNumbers` algorithm went out of range, causing a `null Integer` to be shuffled into the `ArrayList`.  

The programmer decides to use an `ArrayList<Integer>` to store the numbers to be called by the `Caller`,  
but there is an error in the code.

```java
public class Caller
{
    private ArrayList<Integer> numbers;

    public Caller()
    {
        numbers = getList();
        shuffleNumbers();
    }

    /** Returns the numbers 0...90 in order. */
    private ArrayList<Integer> getList()
    { /* implementation not shown */ }

    /** Shuffle the numbers. */
    private void shuffleNumbers()
    { /* implementation not shown */ }
}
```
When the programmer tests the constructor of the Caller class, she gets a NullPointerException.
Which could be the cause of this error?

---
