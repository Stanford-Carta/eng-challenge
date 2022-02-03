**Backend Engineering Challenge: Command-Line Blackjack**

Please write a command-line version of Blackjack, described below.  The user interaction is whether the single player should “hit” or “stand;” everything else is handled by the program.  In addition to your code file, please include a README with:
instructions on how to run your code
any design choices and assumptions you made when building the program
an brief explanation of any tests (automated or manual) you would run to ensure your code works as expected
anything you would like to add if you had more time
documentation of any known bugs that you did not have time to fix

Please spend 1-2 hours on this exercise.  It is okay if you do not finish in time or if there are bugs in your code, but do the best you can.  We will be looking for readable, well-justified code above all else.  You are welcome to use any language you want to complete the challenge.  When you are done, please email mreinstr@stanford.edu and jwasserman@stanford.edu with a zipped folder containing your code and README.  Feel free to reach out with any questions or clarifications.


**Blackjack Rules**
Blackjack is a card game played with a 52-card deck containing:
numbers cards with a value of 2-10 points,
face cards (King, Queen, Jack) each worth 10 points, and
aces, worth either 1 or 11 points
Each deck consists of 4 of each card type listed above.  For the purposes of this game, we will ignore suit.

**Definitions:**
Hand: a collection of cards that a player owns for the duration of the game.
Hit: add another card to a player's hand
Stand: add no more cards to a player's hand; stop playing a turn; proceed to the next phase of the game. 
Bust: more than 21 points in a player's hand; the player's turn is instantly over; the player has lost.
				
**Winning**					
Each player's objective is to get as close to 21 points as possible without going over.
The human wants to outscore the dealer, despite not knowing the dealer's score.
The dealer plays by a simple rule: hit until the hand's score is greater than or equal to 17 ("stand on 17").

**Scoring**
Scoring is just adding the points of a hand together.  Like mentioned above, an Ace can count as either a 1 or 11: whichever makes the hand better.

The game starts with dealing cards. The dealer is dealt two cards: one face up, one face down. The human is then dealt two cards, both face up. Then, the user plays their hand. To do so, they are asked by the program whether to Hit or Stand. The player can continue to hit as many times as they want until they Stand or Bust. When the player chooses to stand their turn is over; they have no further opportunity to get more cards. If at any point the player's score goes over 21, they have busted and lost the game.  If at any point the player gets exactly 21, they instantly win and the game is over.
				
Once the player has stood, the dealer's turn starts. The dealer's hidden card is revealed. The dealer then plays by a simple set of rules: Hit until the hand's score is greater than or equal to 17. If at any time the dealer busts the game is over; the player has won. Otherwise, at some point the dealer will stand. At that point whoever has the highest score wins the game. If both hands have the same score the result is a tie. At this point the game is done, and the program can exit.


**Gameplay Overview**				
1. Deal initial cards (two cards to each player)
2. Display initial hands (hiding dealer's second card and score)
3. Prompt user (Hit or Stand?)
Hit: add card to hand (check if busted)
Stand: end turn
repeat until player has stood, won (score == 21), or busted (score > 21)
4. Dealer plays (if player has neither busted nor won) print dealer's full hand, score dealer keeps hitting until score >= 17
5. Decide and report the winner, including hands and scores where relevant


**Implementation and Program Notes**
You have discretion over the exact details of the user interface. You may also use any programming language with which you are comfortable and can write clean, readable, functional code. Have fun with the program!
