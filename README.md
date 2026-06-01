# Norm of a matrix
## Aim
To write a program to find the 1-norm, 2-norm and infinity norm of the matrix and display the result in two decimal places.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
	1. Get the input matrix using np.array()   
    2. Find the 2-norm of the matrix using np.linalg.norm()
	3. Print the norm of the matrix in two decimal places.
## Program:
```Python

# 1-Norm of a Matrix

'''
 find the 1-Norm of a matrix and display the results in two decimal places.
 developed by:THARUN N
 register number:212225240173
'''

matrix = eval(input())

rows = len(matrix)
cols = len(matrix[0])

one_norm = 0

for j in range(cols):
    col_sum = 0
    for i in range(rows):
        col_sum += abs(matrix[i][j])
    one_norm = max(one_norm, col_sum)

print(f"{one_norm:.2f}")


# 2-Norm of a Matrix
'''
Program to find 2-norm of a matrix.
Developed by: THARUN N
RegisterNumber: 212225240173
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np

A = np.array(eval(input()), dtype=float)

l2_norm = np.linalg.norm(A, 2)

print(f"{l2_norm:.2f}")




# Infinity Norm of a Matrix

'''
program to find the Infinity of a matrix and display the result in two decimal places.
Developed by:THARUN N
Register number:212225240173
'''
# Find the Infinity Norm of a matrix

matrix = eval(input())

inf_norm = max(sum(abs(element) for element in row) for row in matrix)

print(f"{inf_norm:.2f}")



```
## Output:
### 1-Norm of a Matrix
<img width="757" height="547" alt="Screenshot 2026-06-01 234325" src="https://github.com/user-attachments/assets/f6d388c0-c550-48c6-9f87-9ff8ce57b205" />

### 2-Norm of a Matrix
<img width="507" height="591" alt="Screenshot 2026-06-01 234337" src="https://github.com/user-attachments/assets/f40005a4-ba47-423a-9877-c697f56a3757" />

### Infinity Norm of a Matrix
<img width="519" height="522" alt="Screenshot 2026-06-01 234347" src="https://github.com/user-attachments/assets/4137a2b8-283c-4509-a4be-29e2363b7eae" />

## Result
Thus the program for 1-norm, 2-norm and Infinity norm of a matrix are written and verified.
