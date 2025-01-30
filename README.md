# sudoku_cpp
Sudoku is a 9×9 grid-based puzzle where numbers 1 to 9 must appear exactly once in each row, column, and 3×3 subgrid. Given a partially filled board, our goal is to complete it while following these rules.
# Approach - Backtracking
We use Backtracking, a recursive method that tries different possibilities and backtracks when an invalid state is found.

# Algorithm Steps
- Find the first empty cell ('.') in a row-wise manner.
- Try placing numbers 1 to 9 in the cell:
- Check if the number satisfies Sudoku constraints.
- If valid, place the number and move to the next cell.
- If the board is completely filled, return true (solved).
- If no valid number works, reset the cell (backtrack) and try the next possibility.
- If all possibilities fail, return false (no solution).

Checking if a Number is Safe (issafe function)
Before placing a number at (row, col), we check:
   - Row: The number must not already exist in the row.
   - Column: The number must not already exist in the column.
   - 3×3 Subgrid: The number must not exist in its 3×3 box.

Recursive Backtracking (helper function)
- If row == 9, we have successfully filled the board.
- If the current cell is filled, move to the next.
- Try placing numbers 1-9, checking validity, and recursively solving the rest of the board.
- If no solution is found, backtrack by resetting the cell.
