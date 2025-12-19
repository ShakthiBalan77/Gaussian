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

'''
Developed by: Shakthi Balan V
RegisterNumber : 25016098
'''
```
import numpy as np
def gauss_elimination(A,b):
    n=len(b)
    for k in range(n):
        if A[k][k]==0:
            raise ValueError('Zero pivot encountered!')
        for i in range(k+1,n):
            factor=A[i][k]/A[k][k]
            for j in range(k,n):
                A[i][j]=A[i][j]-factor*A[k][j]
            b[i]=b[i]-factor*b[k]
    x=[0]*n
    for i in range(n-1,-1,-1):
        sum_ax=0
        for j in range(i+1,n):
            sum_ax+=A[i][j]*x[j]
        x[i]=(b[i]-sum_ax)/A[i][i]
    return x
a=int(input())
list1=[]
for i in range(a):
    list2=[]
    for j in range(a+1):
        c=int(input())
        list2.append(c)
    list1.append(list2)
list1=np.array(list1)
A=list1[:,:3]
b=list1[:,3]
solution=gauss_elimination(A,b)
print(f"X0 = {solution[0]:.2f} X1 = { solution[1]:.2f} X2 = { solution[2]:.2f}")
        
```

## Output:
<img width="1504" height="804" alt="image" src="https://github.com/user-attachments/assets/3040c9be-6ba4-4654-974e-40dbb71da285" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

