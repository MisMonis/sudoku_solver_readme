# sudoku_solver_readme
**Sudoku solver**

**Project Description**

This is a program which solves any given Sudoku with the help of the solver module. 
The input for the solver is a list of lists (matrix) with 9x9 which is filled with the given numbers 
and 0 for empty spaces. The output will be the solved Sudoku as a list of lists (matrix) with 
no 0 and filled with all numbers so that in each row, column and 3x3 square each number 
only occurs once


**Algorithm**

The chosen algorithm is a backtracking algorithm which is a sort of bruteforce algorithm. 
The following steps will be done:

solve_sudoku():

1. Take the given matrix and search for the next empty field (indicated with 0)
2. Place the number 1 into the field
3. Check if the constraints are fulfilled (every number only once in each row, column 
and square) -> see function check_constraints
    a. if yes -> Repeat steps 1 to 3 for the next fields until constraints are not fulfilled 
    anymore or until every empty field is filled
    b. if no -> go to step 2 and add 1 to the number (change to 2,3,4…9) until 
    constraints are fulfilled again
        i. if constraints cannot be fulfilled anymore (if at 9 cannot be fulfilled), go 
        back one field (last field filled) and add 1 to this number (change to 
        2,3,4…9) until constraints are fulfilled again, then start over with steps 
        1 to 3 for the next field

check_constraints():

matrix [[0,0,0, …],[0,0,0, …],...]

    1. check for each row (e.g. indices first row: matrix[0][0],matrix[0][1],...) if any number 
    between 1 and 9 occurs twice
    2. check for each column (e.g. indices first column: matrix[0][0], matrix[1][0],...] if any 
    number between 1 and 9 occurs twice
    3. check for each square if any number between 1 and 9 occurs twice:
    Computational Management Science WS 21/22
        a. for indices take numbers between 0 and 8 in steps of 3 (0-2, 3-5, 6-8) and 
        check all combinations for first and second index (0-2 and 0-2, 0-2 and 3-5,...)
        
**Installation**
---------------------

**Supported Platforms:** Linux, Windows 10, macOS (both Intel and ARM)
You need also Python3 installed with


**Authors**
Theresa Boiger,
Julian scherr,
Monika Matysiak

**License**
GNU General Public License
