# AI-Assignment-4
### 🧩 Sudoku Solver — CSP with AC-3 & Backtracking

A Python-based Sudoku solver that models the puzzle as a Constraint Satisfaction Problem (CSP), using AC-3 arc consistency and backtracking search to efficiently solve puzzles of varying difficulty levels.

### 📁 Project Structure
├── AI_AS_4.ipynb      # Main solver notebook
├── easy.txt           # Easy difficulty puzzle
├── medium.txt         # Medium difficulty puzzle
├── hard.txt           # Hard difficulty puzzle
└── veryhard.txt       # Very hard difficulty puzzle

### 🧠 How It Works
📌 Modeling as a CSP
Variables: Each cell (row, col) in the 9×9 grid
Domains: Digits 1–9 for empty cells; fixed value for pre-filled cells
Constraints: All cells in the same row, column, or 3×3 box must be distinct
📌 AC-3 (Arc Consistency Algorithm)

Before backtracking begins, AC-3 is applied to reduce domains by removing inconsistent values.
This significantly reduces the search space.

📌 Backtracking Search

A recursive backtracking algorithm:

Assigns values one variable at a time
Checks consistency at each step
If conflict occurs → backtracks and tries another value

### 📊 Results
Puzzle	Backtrack Calls	Backtrack Failures
Easy	1	0
Medium	95	69
Hard	905	851
Very Hard	10892	10836

### ▶️ How to Run
Requirements
Python 3.x
Jupyter Notebook (optional for .ipynb)
Run in Jupyter
jupyter notebook AI_AS_4.ipynb
Run as a Script
python sudoku_solver.py

Make sure all .txt puzzle files are in the same directory.

### 📄 Puzzle Format

Each puzzle is a plain .txt file with 9 lines of 9 digits.
0 represents an empty cell.

Example:

004030050
609400000
005100489
...
### 🔮 Possible Improvements
MRV Heuristic: Choose variable with fewest remaining values
Degree Heuristic: Break ties using most constrained variable
LCV Heuristic: Try least constraining values first
Forward Checking: Propagate constraints immediately after assignment
### 📚 Concepts Used
Constraint Satisfaction Problems (CSP)
Arc Consistency (AC-3)
Backtracking Search
Forward Checking
### 👤 Author

Maidah Nasir
AI / Computer Science Assignment — Sudoku CSP Solver
