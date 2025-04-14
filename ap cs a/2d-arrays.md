1. 1  -2  -6  
   -2   4   5

0. -1   2  -6  
    2  -4   5

0. -1  -2  -6  
   -2  -4  -5

0. 1   2  -6  
   2   4   5

0. 1   2   6  
   2   4   5

A matrix (two-dimensional array) is declared as:
```java
int[][] mat = new int[2][3];
```
Consider the following method:
```java
public static void changeMatrix(int[][] mat)
{
    for (int r = 0; r < mat.length; r++)
        for (int c = 0; c < mat[r].length; c++)
            if (r == c)
                mat[r][c] = Math.abs(mat[r][c]);
}
```
If `mat` is initialized to be:  
-1  -2  -6  
-2  -4   5
Which matrix will be the result of a call to `changeMatrix(mat)`?

---

0. mirrorVerticalLeftToRight  
0. mirrorVerticalRightToLeft  
1. mirrorHorizontalTopToBottom  
0. mirrorHorizontalBottomToTop  
0. mirrorDiagonalRightToLeft  

Consider a program that has a two-dimensional array `mat` of `int` values. The program has several methods that change `mat` by reflecting elements of `mat` across a mirror placed symmetrically on the matrix. Here are five such methods:
```java
mirrorVerticalLeftToRight transforms 
2 4 6    2 4 2
1 3 5 to 1 3 1
8 9 0    8 9 8

mirrorVerticalRightToLeft transforms 
2 4 6    6 4 6
1 3 5 to 5 3 5
8 9 0    0 9 0

mirrorHorizontalTopToBottom transforms 
2 4 6    2 4 6
1 3 5 to 1 3 5
8 9 0    2 4 6

mirrorHorizontalBottomToTop transforms 
2 4 6    8 9 0
1 3 5 to 1 3 5
8 9 0    2 4 6

mirrorDiagonalRightToLeft transforms 
2 4 6    2 4 6
1 3 5 to 4 3 5
8 9 0    6 5 0
```
Consider the following method that transforms the matrix in one of the ways shown above.
```java
public static void someMethod(int[][] mat)
{
    int height = mat.length;
    int numCols = mat[0].length;
    for (int col = 0; col < numCols; col++)
        for (int row = 0; row < height / 2; row++)
            mat[height - row - 1][col] = mat[row][col];
}
```
Which method described above corresponds to someMethod?

---