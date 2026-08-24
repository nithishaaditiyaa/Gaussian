# Gaussian Elimination
Name : R . Nithish Aaditiyaa
 
Register Number : 212225040287

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```

import os
os.environ["OPENBLAS_NUM_THREADS"] = "1"

n = int(input())

a = []
for i in range(n):
    row = []
    for j in range(n + 1):
        row.append(float(input()))
    a.append(row)

for i in range(n):
    for j in range(i + 1, n):
        factor = a[j][i] / a[i][i]
        for k in range(i, n + 1):
            a[j][k] -= factor * a[i][k]

x = [0] * n
for i in range(n - 1, -1, -1):
    x[i] = a[i][n]
    for j in range(i + 1, n):
        x[i] -= a[i][j] * x[j]
    x[i] /= a[i][i]

for i in range(n):
    print(f"X{i} = {x[i]:.2f}", end=" ")

```

## Output:

<img width="1282" height="832" alt="image" src="https://github.com/user-attachments/assets/f2ad6009-f405-4622-bd0c-1fd25f8419ff" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

