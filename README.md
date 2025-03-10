# matlabproject

This project is a MATLAB-based card game implemented using App Designer, where players take turns drawing and placing cards on the table based on matching rules. The key functionalities of the project include:

1. Initialization and Setup
  The game starts with the creation of a deck of playing cards, consisting of different suits (spades, diamonds, hearts, clubs) and ranks (ace, 2 to 10, jack, queen, king).
  The deck is shuffled randomly to ensure fairness.
  The cards are then dealt to both players, with the first 5 cards assigned to the player and the next 5 to the opponent.
  A starting card is placed on the table from the remaining deck.
2. User Interface Components
  The game uses MATLAB App Designer UI components to allow interactions:
    - ListBox (CartiListBox): Displays the player's hand and allows card selection.
    - Buttons:
        "Imparte Carti" (Deal Cards) – Starts a new game.
        "Trage Carte" (Draw Card) – Allows the player to draw a card from the deck.
        "Lasa Carte" (Place Card) – Places the selected card on the table if it follows the rules.
    - Axes (UIAxes):
        Displays card images for the player, the opponent, the deck, and the table.
3. Game Mechanics
- Drawing Cards:
    When the player presses "Trage Carte", a new card is drawn from the deck and added to the player’s hand and the ListBox.
    The deck image updates accordingly.
- Placing Cards on the Table:
    The player selects a card from the ListBox and presses "Lasa Carte".
    A valid move requires that the selected card matches the rank or suit of the card currently on the table.
    If valid, the card is removed from the player's hand, placed on the table, and the opponent's turn begins.
    If invalid, an error message appears.
- Opponent's Turn:
    The opponent checks if they have a valid move.
    If a valid move exists, they place a card on the table.
    If no valid move exists, they draw a card.
4. Image Handling
  The images for the cards are stored in a specific folder.
  Functions handle the display of images when:
    - A card is drawn.
    - A card is placed on the table.
    - The player selects a card from the ListBox.
5. End of the Game
The game ends if:
    - The player has no more cards.
    - The opponent has no more cards.
    - The deck is empty.
A message box (uialert) notifies the player when the game ends.
