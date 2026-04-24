# AI-Assignment-4
# 🧩 Sudoku Solver — CSP with AC-3 & Backtracking
A Python-based Sudoku solver that models the puzzle as a Constraint Satisfaction Problem (CSP), using AC-3 arc consistency and backtracking search to efficiently find solutions across varying difficulty levels.

# 📁 Project Structure
├── AI_AS_4.ipynb       # Main solver notebook
├── easy.txt            # Easy difficulty puzzle
├── medium.txt          # Medium difficulty puzzle
├── hard.txt            # Hard difficulty puzzle
└── veryhard.txt        # Very hard difficulty puzzle

# 🧠 How It Works
1. Modeling as a CSP

Variables: Each cell (row, col) in the 9×9 grid
Domains: Digits 1–9 for empty cells; fixed value for pre-filled cells
Constraints: All cells in the same row, column, or 3×3 box must be distinct

2. AC-3 (Arc Consistency Algorithm)
Before backtracking begins, AC-3 is run to reduce domains by eliminating values that violate binary constraints. This significantly prunes the search space.
3. Backtracking Search
A recursive backtracking algorithm assigns values to variables one at a time, checking consistency at each step. If a conflict is found, it backtracks and tries the next value.

# 📊 Results
---------------------------------------------------
#Puzzle     | Backtrack Calls | Backtrack Failures |
---------------------------------------------------
Easy       | 1               | 0                  | 
Medium     | 95              | 69                 |
Hard       | 905             | 851                |
Very Hard  | 10,892          | 10,836             |

# ▶️ How to Run
Requirements

# Python 3.x
Jupyter Notebook (optional, for .ipynb)

# Run in Jupyter
bashjupyter notebook AI_AS_4.ipynb
Run as a Script
Extract the code from the notebook and run:
bashpython sudoku_solver.py
Make sure all .txt puzzle files are in the same directory.

# 📄 Puzzle Format
Each puzzle is a plain .txt file with 9 lines of 9 digits. 0 represents an empty cell.
004030050
609400000
005100489
...

# 🔮 Possible Improvements

# MRV Heuristic:
Select the variable with the fewest remaining values first to reduce backtracking
# Degree Heuristic:
Break MRV ties by choosing the variable with the most constraints
# LCV Heuristic:
Order values by least constraining value to preserve flexibility
# Full Forward Checking:
Propagate domain reductions immediately after each assignment


# 📚 Concepts Used

Constraint Satisfaction Problems (CSP)
Arc Consistency (AC-3)
Backtracking Search
Forward Checking


# 👤 Author
# Maidah Nasir
AI / Computer Science Assignment — Sudoku CSP Solver
