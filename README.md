# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
## Step 1:
Import the necessary libraries and get input from the user
## Step 2:
Use nested loops to iterate over each element of the matrix
## Step 3:
Perform Gaussian elimination to solve the system of linear equations.
## Step 4: 
Use back Substitution and Print the output
## Program:
```
'''Program to solve a matrix using Gaussian elimination with partial pivoting.
Developed by: Vanitha S
RegisterNumber: 212222100057
'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
X=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
        
for i in range(n):
    if a[i][i] == 0.0:
       sys.exit('Divide by zero detected')

    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
X[n-1]=a[n-1][n]/a[n-1][n-1]  
for i in range(n-2,-1,-1):
    X[i]=a[i][n]
    for j in range(i+1,n):
        X[i]=X[i]-a[i][j]*X[j]
    X[i]=X[i]/a[i][i] 
for i in range(n):
    print('X%d = %0.2f'%(i,X[i]),end=' ')
```

## Output:
![image](https://github.com/Vanitha-SM/Gaussian/assets/119557985/3ca84c49-f858-49db-be13-28de2348d48d)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

