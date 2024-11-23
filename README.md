### Blog Post: My First Python Project: Tic Tac Toe Game

#### Introduction: Why I Built a Tic Tac Toe Game

After experimenting with basic concepts, I wanted to create something that felt engaging and practical—something users could actually play. That’s when I decided to build a **Tic Tac Toe** game. It felt like the perfect challenge to apply my knowledge of functions, loops, conditionals, and lists.

#### How the Code Works

The code for this Tic Tac Toe game is structured around functions that allow players to take turns, mark their positions on the board, and check if someone has won. Here’s a breakdown of the important sections:

1. **Welcome Function**: 
   The game starts by asking the players for their names. This ensures a personal experience as the game addresses each player by their chosen name.

   ```python
   def welcome():
       print("Welcome to Tic Tac Toe game.\nPlease insert the names of the players.")
       player1 = input("Player 1:")
       player2 = input("Player 2:")
       return [player1, player2]
   ```

2. **Menu Function**: 
   This function is responsible for displaying the game board and prompting the player to choose where they want to place their mark ('X' or 'O'). The player selects a position from the available options (labeled 'a' through 'i').

   ```python
   def menu(player):
       print("It's your turn {}, where do you want to play next?".format(player))
       print(game_options)
       return input("Option:")
   ```

3. **Play Function**: 
   This function updates the game board based on the player's selected option, replacing the empty space with the player's mark.

   ```python
   def play(option, current_game, mark):
       ind = game_options.index(option)
       return current_game[:ind] + mark + current_game[ind+1:]
   ```

4. **Winner Check**:
   After every move, the `any_winner` function checks if the current player has achieved a winning combination on the board. The game will end as soon as a player wins or if all spaces are filled (resulting in a tie).

   ```python
   def any_winner(current_game, mark, i):
       # Winning combinations
       winning_combinations = [['a','b','c'],['d','e','f'],['g','h','i'],['a','d','g'],['b','e','h'],['c','f','i'],['a','e','i'],['c','e','g']]
       ...
       for w_comb in winning_combinations:
           if w_comb[0] in played_combinations[i] and w_comb[1] in played_combinations[i] and w_comb[2] in played_combinations[i]:
               return True
       return False
   ```

The game runs in a loop until a player wins or the board is full, resulting in a tie. The board is printed after every turn to keep the players updated on the game’s progress.

#### Link to the Code

If you want to check out the full Python code, feel free to explore it on [GitHub](https://github.com/sofiatmenezes/tic-tac-toe).

#### Conclusion: What I Learned

Creating this Tic Tac Toe not only allowed me to gain a deeper understanding of functions and conditionals in Python, but I also learned how to implement simple interactive programs that users can engage with. It helped me build a strong foundation in coding, and it was a lot of fun to see the game come to life. As I continue my Python journey, I look forward to taking on more complex projects and improving my coding skills.
