# blackjack_Analysis
Analysis of Probability of winning, tie or losing a hand at blackjack.

The code simulates a game of blackjack for a given number of stacks, where each stack is an independent round of the game, and each stack is played by a given number of players with a specified number of decks of cards.

The code first defines some functions that are used in the game, such as get_ace_val that returns a list of possible values for a hand that contains one or more aces, make_dck that creates a deck of cards with a given number of decks and card type, and total_up that calculates the total value of a hand.

Then the code simulates a game of blackjack for each stack. In each game, the code deals two cards to each player and the dealer, and the players hit or stand based on a basic strategy that depends on their current hand value and the dealer's up-card. The dealer hits until they have a hand value of 17 or higher. The players win if their hand value is higher than the dealer's and does not exceed 21, or if the dealer busts (exceeds 21). The players lose if their hand value exceeds 21 or is lower than the dealer's. If a player or the dealer has a hand value of 21 with two cards (an Ace and a 10-value card), they have a blackjack and win immediately, unless the dealer also has a blackjack.

The code keeps track of the results of each player for each round of the game, and at the end of each round, it calculates the average winnings/losses for each player over all rounds. The results are stored in plr_results.

The player hits based on the basic blackjack strategy defined in the code, which considers the player's total hand value and the dealer's up card.

For example, if the player's total hand value is less than 12, the player hits until the total hand value is 12 or greater. If the player's total hand value is exactly 12 and the dealer's up card is 2, 3, 7, 8, 9, or 10, the player hits. If the player's total hand value is between 13 and 16 (inclusive) and the dealer's up card is 2, 3, 4, 5, or 6, the player hits. If the player's total hand value is exactly 17 and the dealer's up card is 2, 3, 4, 5, 6, or 7, the player hits. If the player's total hand value is 18 or greater, the player stands (does not hit).


Reference for hitting and staying was used from https://blog.betway.com/casino/blackjack-strategy-101-what-is-the-hit-stand-betting-system/.
