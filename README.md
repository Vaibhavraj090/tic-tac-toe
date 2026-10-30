def print_board(board):
    """Prints the current state of the game board."""
    print("\n")
    print(f" {board[0]} | {board[1]} | {board[2]} ")
    print("---|---|---")
    print(f" {board[3]} | {board[4]} | {board[5]} ")
    print("---|---|---")
    print(f" {board[6]} | {board[7]} | {board[8]} ")
    print("\n")

def check_win(board, player):
    """Checks if the given player has won the game."""
    win_conditions = [
        [0, 1, 2], [3, 4, 5], [6, 7, 8],  # Rows
        [0, 3, 6], [1, 4, 7], [2, 5, 8],  # Columns
        [0, 4, 8], [2, 4, 6]              # Diagonals
    ]
    for condition in win_conditions:
        if board[condition[0]] == board[condition[1]] == board[condition[2]] == player:
            return True
    return False

def check_draw(board):
    """Checks if the board is completely full (a draw)."""
    return all(space in ['X', 'O'] for space in board)

def play_game():
    """Main function to run the Tic-Tac-Toe game loop."""
    # Initialize the board with position numbers 1-9
    board = [str(i) for i in range(1, 10)]
    current_player = "X"
    
    print("Welcome to Tic-Tac-Toe!")
    print("Players take turns entering a position number (1-9) to place their mark.")
    
    while True:
        print_board(board)
        
        # Get input and handle potential errors
        try:
            choice = int(input(f"Player {current_player}'s turn. Choose a position (1-9): "))
        except ValueError:
            print("Invalid input. Please enter a number between 1 and 9.")
            continue
            
        # Validate entry boundary
        if choice < 1 or choice > 9:
            print("Out of range. Please choose a number between 1 and 9.")
            continue
            
        # Check if the space is already taken
        index = choice - 1
        if board[index] in ['X', 'O']:
            print("That position is already taken! Try a different spot.")
            continue
            
        # Place the mark
        board[index] = current_player
        
        # Check game status
        if check_win(board, current_player):
            print_board(board)
            print(f"Congratulations! Player {current_player} wins! 🎉")
            break
            
        if check_draw(board):
            print_board(board)
            print("It's a draw! Well played. 🤝")
            break
            
        # Swap players
        current_player = "O" if current_player == "X" else "X"

if __name__ == "__main__":
    play_game()
