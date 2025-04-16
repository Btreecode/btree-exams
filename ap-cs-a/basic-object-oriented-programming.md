1. suit = cardSuit;  
   value = cardValue;
0. cardSuit = suit;  
   cardValue = value;
0. Card = new Card(suit, value);
0. Card = new Card(cardSuit, cardValue);
0. suit = getSuit();  
   value = getValue();

```java
public class Card
{
    private String suit;
    private int value;  // 0 to 12

    public Card(String cardSuit, int cardValue)
    { /* implementation */ }

    public String getSuit()
    {
        return suit;
    }

    public int getValue()
    {
        return value;
    }

    public String toString()
    {
        String faceValue = "";
        if (value == 11)
            faceValue = "J";
        else if (value == 12)
            faceValue = "Q";
        else if (value == 0)
            faceValue = "K";
        else if (value == 1)
            faceValue = "A";

        if (value >= 2 && value <= 10)
            return value + " of " + suit;
        else
            return faceValue + " of " + suit;
    }
}

public class Deck
{
    private Card[] deck;
    public final static int NUMCARDS = 52;

    public Deck()
    {
        ...
    }

    /** Simulate shuffling the deck. */
    public void shuffle()
    {
        ...
    }
    // Other methods are not shown.
}
```
Which of the following represents correct `/* implementation */` code for the constructor in the `Card` class?

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

0. I only  
0. II only  
0. III only  
0. I and II only  
1. I, II, and III  

Which of the following statements about the `Point`, `Quadrilateral`, and `Rectangle` classes are false?

I. `Point` is a subclass of `Quadrilateral`.  
II. `Point` is a subclass of `Rectangle`.  
III. The `Rectangle` class inherits the constructor of `Quadrilateral`.

```java
public class Point
{
    private int xCoord;
    private int yCoord;

    // constructor
    public Point(int x, int y)
    {
        ...
    }

    // accessors
    public int get_x()
    {
        ...
    }

    public int get_y()
    {
        ...
    }

    // Other methods are not shown.
}

public class Quadrilateral
{
    private String labels;    // e.g., "ABCD"

    // constructor
    public Quadrilateral(String quadLabels)
    {
        labels = quadLabels;
    }

    public String getLabels()
    {
        return labels;
    }

    public int perimeter()
    {
        return 0;
    }

    public int area()
    {
        return 0;
    }
}

public class Rectangle extends Quadrilateral
{
    // coords of top left corner
    private Point topLeft;

    // coords of bottom right corner
    private Point botRight;

    // constructor
    public Rectangle(String theLabels, Point theTopLeft, Point theBotRight)
    {
        /* implementation code */
    }

    public int perimeter()
    {
        /* implementation not shown */
    }

    public int area()
    {
        /* implementation not shown */
    }

    // Other methods are not shown.
}
```

---

0. I only  
0. II only  
1. III only  
0. I and II only  
0. II and III only  

Which represents correct `/* implementation code */` for the `Rectangle` constructor?

I. `super(theLabels);`  
II. `super(theLabels, theTopLeft, theBotRight);`  
III. `super(theLabels);  
     topLeft = theTopLeft;  
     botRight = theBotRight;`

```java
public class Point
{
    private int xCoord;
    private int yCoord;

    // constructor
    public Point(int x, int y)
    {
        ...
    }

    // accessors
    public int get_x()
    {
        ...
    }

    public int get_y()
    {
        ...
    }

    // Other methods are not shown.
}

public class Quadrilateral
{
    private String labels;    // e.g., "ABCD"

    // constructor
    public Quadrilateral(String quadLabels)
    {
        labels = quadLabels;
    }

    public String getLabels()
    {
        return labels;
    }

    public int perimeter()
    {
        return 0;
    }

    public int area()
    {
        return 0;
    }
}

public class Rectangle extends Quadrilateral
{
    // coords of top left corner
    private Point topLeft;

    // coords of bottom right corner
    private Point botRight;

    // constructor
    public Rectangle(String theLabels, Point theTopLeft, Point theBotRight)
    {
        /* implementation code */
    }

    public int perimeter()
    {
        /* implementation not shown */
    }

    public int area()
    {
        /* implementation not shown */
    }

    // Other methods are not shown.
}
```

---

1. The area of each Quadrilateral in quadList will be printed.  
0. A value of 0 will be printed for each element of quadList.  
0. A compile-time error will occur, stating that there is no getLabels method in classes Rectangle, Parallelogram, or Square.  
0. A NullPointerException will be thrown.  
0. A ConcurrentModificationException will occur.  

Refer to the Parallelogram and Square classes below.

```java
public class Parallelogram extends Quadrilateral
{
    //Private instance variables and constructor are not shown.
    ...

    public int perimeter()
    { /* implementation not shown */ }

    public int area()
    { /* implementation not shown */ }
}

public class Square extends Rectangle
{
    //Private instance variables and constructor are not shown.
    ...

    public int perimeter()
    { /* implementation not shown */ }

    public int area()
    { /* implementation not shown */ }
}
```

Consider an `ArrayList<Quadrilateral> quadList` whose elements are of type `Rectangle`, `Parallelogram`, or `Square`.
Refer to the following method, `writeAreas`:
```java
/** Precondition: quadList contains Rectangle, Parallelogram, or
  * Square objects in an unspecified order.
  */

public static void writeAreas(ArrayList<Quadrilateral> quadList)
{
    for (Quadrilateral quad : quadList)
        System.out.println("Area of " + quad.getLabels()
            + " is " + quad.area());
}
```
What is the effect of executing this method?

---

1. `return (int) (getValue() - 0.5);`  
0. `return (int) (getValue() + 0.5);`  
0. `return (int) getValue();`  
0. `return (double) (getValue() - 0.5);`  
0. `return (double) getValue();`  

Consider the `NegativeReal` class below, which defines a negative real number object.

```java
public class NegativeReal
{
    private Double negReal;

    /** Constructor. Creates a NegativeReal object whose value is num.
     *  @param num a negative real number
     */
    public NegativeReal(double num)
    { /* implementation not shown */ }

    /** @return the value of this NegativeReal */
    public double getValue()
    { /* implementation not shown */ }

    /** @return this NegativeReal rounded to the nearest integer */
    public int getRounded()
    { /* implementation */ }
}
```
| Negative real number | Rounded to nearest integer |
|----------------------|-----------------------------|
| -3.5                 | -4                          |
| -8.97                | -9                          |
| -5.0                 | -5                          |
| -2.487               | -2                          |
| -0.2                 | 0                           |
Which `/* implementation */` of `getRounded` produces the desired postcondition?

---

0. None  
0. I only  
0. II only  
0. III only  
1. I and II only  

Refer to the definitions of `ClassOne` and `ClassTwo` below.

```java
public class ClassOne
{
    public void methodOne()
    {
        ...
    }

    // Other methods are not shown.
}

public class ClassTwo extends ClassOne
{
    public void methodTwo()
    {
        ...
    }

    // Other methods are not shown.
}
```
Consider the following declarations in a client class.
You may assume that ClassOne and ClassTwo have no-argument constructors.
```java
ClassOne c1 = new ClassOne();
ClassOne c2 = new ClassTwo();
```
Which of the following method calls will cause an error?
```java
I. c1.methodTwo();
II. c2.methodTwo();
III. c2.methodOne();
```

---

0. It sums the elements of `arr`.  
0. It sums the products 10 * arr[0] + 10 * arr[1] + ⋯ + 10 * arr[arr.length - 1].  
1. It builds an integer of the form d₁d₂d₃...dₙ, where d₁ = arr[0], d₂ = arr[1], ..., dₙ = arr[arr.length - 1].  
0. It builds an integer of the form d₁d₂d₃...dₙ, where d₁ = arr[arr.length - 1], d₂ = arr[arr.length - 2], ..., dₙ = arr[0].  
0. It converts the elements of arr to base-10.  

Refer to the following class containing the `mystery` method:

```java
public class SomeClass
{
    private int[] arr;

    /** Constructor. Initializes arr to contain nonnegative
     * integers k such that 0 <= k <= 9.
     */
    public SomeClass()
    { /* implementation not shown */ }

    public int mystery()
    {
        int value = arr[0];
        for (int i = 1; i < arr.length; i++)
            value = value * 10 + arr[i];
        return value;
    }
}
```
Which best describes what the `mystery` method does?

---

0. procedural abstraction  
0. data encapsulation  
1. composition  
0. inheritance  
0. independent classes  

A programmer plans to write a program that simulates a small bingo game (no more than six players). Each player will have a bingo card with 20 numbers from 0 to 90 (no duplicates). Someone will call out numbers one at a time, and each player will cross out a number in their card as it is called. The first player with all the numbers crossed out is the winner. In the simulation, the game is in progress, each player’s card is displayed on the screen.

The programmer envisions a short driver class whose main method has just two statements:
```java
BingoGame b = new BingoGame();
b.playBingo();
```
The BingoGame class will have several objects: a PlayerGroup, a Caller, and a PlayerGroup. The PlayerGroup will have a list of Players, and each Player will have a BingoCard.

The relationship between the PlayerGroup and Player classes is an example of

---

0. tiles.set(size, temp);  
   tiles.set(index, tiles.get(size));
1. tiles.set(index, tiles.get(size));  
   tiles.set(size, temp);
0. tiles.swap(index, size);
0. tiles.get(size, temp);  
   tiles.get(index, tiles.set(size));
0. tiles.get(index, tiles.set(size));  
   tiles.get(size, temp);

A word creation game uses a set of small letter tiles, all of which are initially in a tile bag. A partial implementation of a `TileBag` class is shown below.

```java
public class TileBag
{
    // tiles contains all the tiles in the bag
    private ArrayList<Tile> tiles;

    // size is the number of not-yet-used tiles
    private int size;

    // Constructors and other methods are not shown.
}
```
Consider the following method in the `TileBag` class that allows a player to get a new tile from the `TileBag`.
```java
public Tile getNewTile()
{
    if (size == 0) // no tiles left
        return null;

    int index = (int)(Math.random() * size);
    size--;
    Tile temp = tiles.get(index);

    /* code to swap tile at position size with tile at position index */

    return temp;
}
```
Which /* code to swap tile at position size with tile at position index */ performs the swap correctly?

---

1. The algorithm allows the program to keep track of both used and unused tiles.
0. The tiles list becomes one element shorter when `getNewTile` is executed.
0. The algorithm selects a random Tile from all tiles in the list.
0. The tiles list has used tiles in the beginning and unused tiles at the end.
0. The tiles list contains only tiles that have not been used.

A word creation game uses a set of small letter tiles, all of which are initially in a tile bag. A partial implementation of a `TileBag` class is shown below.
```java
public class TileBag
{
    // tiles contains all the tiles in the bag
    private ArrayList<Tile> tiles;

    // size is the number of not-yet-used tiles
    private int size;

    // Constructors and other methods are not shown.
}
```
Consider the following method in the `TileBag` class that allows a player to get a new tile from the `TileBag`.
```java
public Tile getNewTile()
{
    if (size == 0) // no tiles left
        return null;

    int index = (int)(Math.random() * size);
    size--;
    Tile temp = tiles.get(index);

    /* code to swap tile at position size with tile at position index */

    return temp;
}
```
Which is true about the `getNewTile` algorithm?

---

0. fly  
0. fly chirp  
0. fly chirp waddle  
0. fly chirp waddle coo  
1. fly chirp coo waddle  

Consider the following two classes.

```java
public class Bird {
    public void act() {
        System.out.print("fly ");
        makeNoise();
    }

    public void makeNoise() {
        System.out.print("chirp ");
    }
}

public class Dove extends Bird {
    public void act() {
        super.act();
        System.out.print("waddle ");
    }

    public void makeNoise() {
        super.makeNoise();
        System.out.print("coo ");
    }
}
```
Suppose the following declaration appears in a class other than Bird or Dove:
```java
Bird pigeon = new Dove();
```
What is printed as a result of the call pigeon.act()?

---
