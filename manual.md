# Lucky 21 - User Manual

## Starting the Application

Open the project in IntelliJ IDEA or another Java IDE and run `src/Main.java`.

The console application starts with 100 chips. You can use the keyboard to enter numbers or answers.

## Starting a Round

At the beginning of each round, the application displays your current chip balance and asks:

```text
Enter bet (0 to end):
```

Enter an integer between `0` and your current chip balance:

- Enter a positive amount to place a bet.
- Enter `0` to leave the game.
- Invalid values are rejected with an instruction to enter a valid bet.

## Playing a Round

Your cards and the dealer's cards are shown as a table. The dealer's first card is hidden during the player's turn and shown as `??`.

Choose an action by entering:

- `1` — Draw one more card.
- `2` — Hold and end your turn.
- `3` — Quit the game immediately.

After drawing a card, the application recalculates and displays your point total. You can continue drawing or hold while your score is 21 or less. A score above 21 loses the round.

## Card Values

- Number cards `2` through `10` keep their number value.
- `J`, `Q`, and `K` are worth 10 points.
- An ace is worth 11 points and is reduced to 1 point when necessary to avoid exceeding 21.

## Dealer Turn and Results

After you hold, the dealer reveals the hidden card. The dealer draws until reaching at least 17 points.

The application recognizes:

- Blackjack
- A win
- A loss
- A tie
- A dealer bust

A win returns the original bet plus winnings. A tie returns the original bet. A loss removes the bet from the chip balance.

## Continuing or Ending

After a completed round, enter:

- `y` or `yes` to play another round.
- `n` or another answer to end the game.

The game also ends when your chip balance reaches zero or when you enter `0` at the bet prompt or select `3` during a round.
