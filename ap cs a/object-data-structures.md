0. I only  
0. II only  
0. III only  
0. I and II only  
1. I, II, and III  

A programmer plans to write a program that simulates a small bingo game (no more than six players). Each player will have a bingo card with 20 numbers from 0 to 90 (no duplicates). Someone will call out numbers one at a time, and each player will cross out a number in their card as it is called. The first player with all the numbers crossed out is the winner. In the simulation, the game is in progress, each player’s card is displayed on the screen.

The programmer envisions a short driver class whose main method has just two statements:
```java
BingoGame b = new BingoGame();
b.playBingo();
```
The BingoGame class will have several objects: a PlayerGroup, a Caller, and a PlayerGroup. The PlayerGroup will have a list of Players, and each Player will have a BingoCard.

Which is a reasonable data structure for a `BingoCard` object? Recall that there are 20 integers from 0 to 90 on a `BingoCard`, with no duplicates. There should also be mechanisms for crossing off numbers that are called and for detecting a winning card (i.e., one where all the numbers have been crossed off).

**I.**  
```java
int[] bingoCard;  // Will contain 20 integers  
// A number is crossed off by setting it to -1  
int numCrossedOff;  // Player wins when numCrossedOff reaches 20
```
**II.**
```java
boolean[] bingoCard; // Will contain 91 boolean values , of which 20 are true. All the other values are false.
// Thus, if bingoCard[k] is true, then k is on the card (0 <= k <= 90)  
// A number  k is crossed off by changing the value of bingoCard[k] to false  
int numCrossedOff;  // Player wins when numCrossedOff reaches 20.
```
**III.**
```java
ArrayList<Integer> bingoCard;  
// Will contain 20 integers  
// A number is crossed off by removing it from the ArrayList  
// Player wins when bingoCard.size() == 0
```

---





