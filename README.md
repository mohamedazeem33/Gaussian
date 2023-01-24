# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
Step1 :
Import the numpy module to use the built-in functions for calculation
<br>
Step 2:
Prepare the lists from each linear equations and assign in np.array()
<br>
Step 3:
Using the np.linalg.eig(), we get two results (first is eigenvalue and second is eigenvector) of the
given matrix.
<br>
Step 4:
End the program

## Program:
```
Developed by: MOHAMED AZEEM N
RegisterNumber: 22007405

import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][j]==0.0:
        sys.exit("Divide by zero detected!")
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio*a[i][k]
x[n-1] = a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=' ')
    
```

## Output:

![Screenshot (78)](https://user-images.githubusercontent.com/121040764/213400208-d4352552-4fe8-4dc1-a60a-6ff199b4586f.png)


## Result:
the Gaussian Elimination  is successfully solved using python program.

