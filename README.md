# How To Submit

- Create a repo(private) using this repo as template in this organization itself
    - Repo name should be your Team/nick_name followed by Language you choose ex: CodeDevil_Java
    - Make sure you had selected Java_Yatzy as template


![image](https://media.github.ford.com/user/18948/files/78e18ebe-6874-496f-bc6d-456b9f8da52f)

- Complete the refactorings and commit your code on the new repo created by you

# Java Yatzy

Yatzy is a popular dice game. It is a game of chance and strategy, played with five dice.  The objective of Yatzy is to score points by rolling specific combinations of dice in a serious of turns. The player with the highest total score at the end of the game wins.

The players take turns rolling five dice with the goal of achieving specific combinations to score points. Each player has a scoresheet where they record their scores for each combination. The following are the 15 rounds of Yatzy


-    Ones
-    Twos
-    Threes
-    Fours
-    Fives
-    Sixes
-    Three of a Kind
-    Four of a Kind
-    Full House
-    Pair
-    Two Pair
-    Small Straight
-    Large Straight
-    Yatzy
-    Chance

#### Game Rules



 *Example*
 A player rolls 5,6,5,5,2 and scores the dice in the fives category they would score 15 (three fives). <br>

#### Yatzy Categories and Scoring Rules <br>

**Rolling the Dice:** <br>
In each turn, a player gets up to two rolls of the five dice.<br> 
After each roll, the player can choose to keep or re-roll any number of dice.<br>


**Rules for reroll:**<br>

After rolling the dice at once and the player is not satisfied with the outcome for choosing the category, the player can opt for reroll. The player can choose only two of the previous dice to reroll but the player could use this reroll opportunity only once for each turn.<br>

*Example :*<br>
Roll dice: 1,3,1,2,4<br>
Reroll: [0,4] - It will select dice values 1,4 for reroll by its index<br>
Dice after reroll: 2,3,1,2,2 <br>
Choose category: Twos<br>
Score: 6<br>

**Criterias in current program:**<br>
- It is a two player game.<br>
- Each player has to roll the dice. The other player will get the turn only when the first player has chosen the category for adding score.<br>
- The player will be allowed to choose each category only once.<br>
- The player can opt for reroll before choosing the category.<br>
- The game will end only if all the categories are chosen by both players. After selecting all categories, the winner will be decided based upon the final score.<br>


**Scoring Combinations:**<br> 
Players aim to achieve specific combinations with the five dice. Here are the common combinations and their scoring rules:<br>

- **Ones, Twos, Threes, Fours, Fives, and Sixes:** <br>
The player's score is the sum of the corresponding number of dice showing that value. For example, if a player rolls 3, 4, 2, 4, 6, they can score 8 points for the two fours.

*Example*<br>

|  Rolls  | Selected Combinations  |  Score |
| ------------ | ------------ | ------------ |
|   3,1,1,2,6 | Ones  |  2 (1+1)  |
|   2,3,2,5,1|  Twos | 4 (2+2)  |
|  3,3,3,4,5 |  Threes | 9 (3+3+3)  |
|   1,1,2,4,4|  Fours |  8 (4+4) |
|   2,3,5,5,6| Fives  |  10 (5+5) |
|   6,1,2,4,6|  Sixes |  12 (6+6) |

- **Three of a kind:**<br>
The player's score is the sum of the three dice if there are exactly three dice with the same number.
If there are not exactly three dice with the same number, the score is 0.<br>

   Example: 3,3,3,4,5 scores 9 (3+3+3)<br>
   Example: 3,3,4,5,6 scores 0 <br>
   Example: 3,3,3,3,1 scores 0  <br>

- **Four of a kind:**<br>
 The player's score is the sum of the four dice if there are exactly four dice with the same number.
  If there are not exactly four dice with the same number, the score is 0.<br>

   Example: 2,2,2,2,5 scores 8 (2+2+2+2) <br>
   Example: 2,2,2,5,5 scores 0   <br>
   Example: 2,2,2,2,2 scores 0 <br>
   
- **Full house:** <br>
The player's score is the sum of all five dice if the dice are two of a kind and three of a different kind.<br>

   Example: 1,1,2,2,2 scores 8 (1+1+2+2+2)<br>
   Example 3: 4,4,4,4,4 scores 0<br>
   
- **Pairs:** <br>
The player's score is the sum of the two highest matching dice if exactly two dice have the same value.<br>

   Example: 3,3,3,4,4 scores 8 (4+4)<br>
   Example: 1,1,6,2,6 scores 12 (6+6)<br>
   Example: 3,3,3,4,1 scores 0  - Although there are three 3s, there is no pair of two matching dice. Therefore, the score is 0.<br>
   Example: 3,3,3,3,1 scores 0  - Similarly, even though there are four 3s, there is no pair. Hence, the score is 0.<br>
   
- **Two pairs:** <br>
The player's score is the sum of four dice if exactly two dice have the same value and exactly two dice have a different value.<br>

   Example: 1,1,2,3,3 scores 8 (1+1+3+3)<br>
   Example: 1,1,2,3,4 scores 0  - In this scenario, there is only one pair (two 1s), and the other dice are not forming a different pair<br>
   Example: 1,1,2,2,2 scores 0  - Here, there's only one pair (two 1s), and the other dice are not forming a different pair.<br>
   
- **Small straight:**<br>
   Score 15 if the dice read 1,2,3,4,5 (consecutive sequence).<br>
   
   Example: 1,2,3,4,5 placed on "small straight" scores 15<br>

- **Large straight:** <br>
   Score 20 if the dice read 2,3,4,5,6 (consecutive sequence).<br>
 
   Example: 2,3,4,5,6 placed on "large straight" scores 20<br>
   
- **Yatzy:**<br>
   Score 50 points if all dice have the same number.<br>
   
   Example: 1,1,1,1,1 placed on "yatzy" scores 50<br>
   Example: 5,5,5,5,5 placed on "yatzy" scores 50<br>   
   Example: 1,1,1,2,1 placed on "yatzy" scores 0<br>
   
- **Chance:**<br>
   Score the sum of all dice.<br>
   
   Example: 1,1,3,3,6 placed on "chance" scores 14 (1+1+3+3+6)<br>
   Example: 4,5,5,6,1 placed on "chance" scores 21 (4+5+5+6+1)<br>


#### Refactoring Opportunities
- No functional way of programming
- There are many duplicated fragments available across the code.
- Conditional and cognitive complexities are high *Not adequate test cases

## Scope for improvements
- Currently there are only two chances of rolling is given to players it can be increased to 3 (1 actual roll + 2 Re rolls) (2 points)
- Implement the single player mode (versus computer - system will choose the combination - implement best Alogorithm for that)(5 points)
- Combinations can be choosen dynamically when the game starts(now players need to play all 15 combinations instead they can choose what are the combinations they want to play)(3 points)
###### * Add neccessary Test cases

# Happy Refactoring !
