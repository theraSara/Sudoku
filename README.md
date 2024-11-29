# Sudoku Solver

This Python program solves a 9x9 Sudoku puzzle using a backtracking algorithm. The program includes functions to validate the board, find empty cells, and recursively solve the puzzle.

## Features
- Validates Sudoku rules (row, column, and 3x3 subgrid constraints).
- Uses backtracking to solve the puzzle efficiently.
- Prints the initial and solved Sudoku board.

---

## How It Works
### Main Functions
1. **`find_empty(bo)`**
   - Locates the first empty cell (value 0) in the board.
   - Returns the position as a tuple `(row, col)`. If no empty cells are found, returns `None`.

2. **`validate(bo, num, pos)`**
   - Checks if placing `num` at `pos` is valid according to Sudoku rules.
   - Ensures:
     - No duplicates in the row or column.
     - No duplicates in the 3x3 subgrid.

3. **`solve(bo)`**
   - Implements a recursive backtracking algorithm to solve the Sudoku.
   - Fills empty cells with numbers 1-9 and backtracks when a conflict arises.

4. **`print_board(bo)`**
   - Displays the Sudoku board in a formatted manner.

---

### Example Input and Output

#### Input Board
```plaintext
7 8 0 | 4 0 0 | 1 2 0
6 0 0 | 0 7 5 | 0 0 9
0 0 0 | 6 0 1 | 0 7 8
- - - - - - - - - - - -
0 0 7 | 0 4 0 | 2 6 0
0 0 1 | 0 5 0 | 9 3 0
9 0 4 | 0 6 0 | 0 0 5
- - - - - - - - - - - -
0 7 0 | 3 0 0 | 0 0 2
1 2 0 | 0 0 7 | 4 0 0
0 4 9 | 2 0 6 | 0 0 7
```
#### Solved Output
```plaintext
7 8 5 | 4 3 9 | 1 2 6
6 1 2 | 8 7 5 | 3 4 9
4 9 3 | 6 2 1 | 5 7 8
- - - - - - - - - - - -
8 5 7 | 9 4 3 | 2 6 1
2 6 1 | 7 5 8 | 9 3 4
9 3 4 | 1 6 2 | 7 8 5
- - - - - - - - - - - -
5 7 8 | 3 9 4 | 6 1 2
1 2 6 | 5 8 7 | 4 9 3
3 4 9 | 2 1 6 | 8 5 7
```

## How to Run?
1. Clone the repository or copy the code.
2. Ensure python 3.x is installed on your system.
3. Run the script in you terminal or IDE:
   ```
   python sudoku_solver.py
   ```
4. The program will display the solved Sudoku board.
