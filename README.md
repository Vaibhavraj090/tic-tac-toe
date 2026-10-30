# tic-tac-toe
# 🎮 Python Tic-Tac-Toe Game

A clean, interactive **Tic-Tac-Toe game built entirely in Python**. This project features a complete implementation of the classic 3x3 grid game, supporting turn-based logic, winner evaluation, tie detection, and user input validation.

## ✨ Features
* **Interactive Gameplay:** Play the classic 3x3 turn-based match with a friend on a shared device.
* **Input Validation:** Error-handling prevents players from selecting already occupied spots or entering invalid inputs.
* **Automatic Win & Tie Detection:** Evaluates horizontal, vertical, and diagonal alignments after every turn.
<!-- Optional Feature Bullets (Keep what applies to your project) -->
* **[Optional] Graphical User Interface (GUI):** Built using `Tkinter` / `Pygame` for clean visual rendering and easy mouse-click interactions.
* **[Optional] Smart AI Opponent:** Play solo against an AI utilizing the Minimax algorithm for an unbeatable challenge.
* **[Optional] Score Tracker:** Tracks player wins across multiple rounds during the session.

## 🛠️ Prerequisites & Installation

### Option A: Command Line / Tkinter (Standard Library)
No external libraries are required if your game relies entirely on Python's built-in modules (`Tkinter` or console output). 

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd YOUR-REPO-NAME
   ```

2. **Run the game:**
   ```bash
   python main.py
   ```

### Option B: Pygame Version
If you built the game using **Pygame**:

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd YOUR-REPO-NAME
   ```

2. **Install dependencies:**
   ```bash
   pip install pygame
   ```

3. **Run the game:**
   ```bash
   python main.py
   ```

## 🎮 How to Play
1. **Player X** always takes the first turn.
2. Choose your grid position:
   * *For CLI:* Input the corresponding number (1-9) or coordinate for the spot you want to claim.
   * *For GUI:* Click directly on the grid square where you want to place your token.
3. The game will automatically detect if a player achieves 3 in a row or if the board runs out of spaces, ending in a draw.
4. Follow the prompt on the screen to reset the board and play again!

## 📂 Project Structure
```text
├── main.py          # The entry point of the game application
├── game_logic.py    # Game mechanics, turn counters, and win-checks (if separated)
├── README.md        # Project documentation
└── assets/          # (Optional) Images, sounds, or style templates
```

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
