# Gaussian Elimination

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
/*
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: G.SANTHIYA
RegisterNumber: 25017564
'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit("Divide by zero detected!")
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end=" ")
*/
```
## Output:
<img width="1455" height="562" alt="image" src="https://github.com/user-attachments/assets/ec64012f-1504-4ecb-8ab9-eb4fb5e7d624" />
<img width="1414" height="652" alt="image" src="https://github.com/user-attachments/assets/47aa7e47-7192-49f4-bdef-1d07d802cf1d" />
<img width="1469" height="607" alt="image" src="https://github.com/user-attachments/assets/d249f737-b725-4783-a46f-e115b0ab5ee4" />

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

