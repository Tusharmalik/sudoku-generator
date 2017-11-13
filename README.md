# sudoku-generator

This program will help in generating different solutions for perfect square matrices.

Sudoku Generator Logic

Major Rules we are focusing:

- The number should not exist already in current row.
- The number should not exist already in current column.
- Number should not exist in the nxn submatrix when matrix is sqr(n)*sqr(n).

Approach is completely based on the Rules:

- We are taking a matrix of n*n size having value `none` in each block

- There is a list of numbers which can be placed in the sudoku code
```
eg: for 2*2 matrix
number = [1,2,3,4]
counter = 0 

Let matrix row be j and matrix column be i
```
- The first row in sudoku code is generated randomly from the `number` list
- From the second row to the nth row(for 4*4 n will be 2) we will check weather the number is present in the current grid or not
- If the number is present in the current grid. Make counter++ 
- Else list[i][j] = number[counter] and pop(number[counter]) 
