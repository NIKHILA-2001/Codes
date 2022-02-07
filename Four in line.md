**Finding 4 consecutive elements of the same value either horizontally,vertically or diagonally.</br>**
**-->if there are more than 1 such elements: print min value</br>**
**-->if there are no such elements : print -1**

#### Input Format</br>
```
n - no of rows 
n lines containing the elements of matrix.Each line will have m elements seperated by space. 
```
**Code(Python)**
``` py
n=int(input())
1st=[]
out=[]
for i in range(n):
  1st.append(input().split())
m=len(1st [0])
for i in range(n):
  for j in range (m-4+1):
    if len(set([lst[i][j],lst[i][j+1],lst[i][j+2],lst[i][j+3]]))==1: 
      out.append(lst[i][j])
for j in range(m):
  for i in range(n-4+1):
    if len(set([lst[i][j],lst[i+1][j],lst[i+2][j],lst[i+3][j]]))==1:
      out.append(lst [i][j])
for i in range(n-4+1):
  for j in range (m-4+1):
    if len(set([lst[i][j],lst[i+1][j+1],lst[i+2][j+2],lst[i+3][j+3]]))==1: 
      out.append (lst[i][j])
for i in range(n-4+1):
  for j in range (m-1,2,-1):
    if len(set([lst[i][j],lst[i+1][j-1],lst[i+2][j-2],lst[i+3][j-3]]))==1: 
      out.append(lst [i][j])

if len(out)==0:
  print("-1")
else:
  print(sorted(out)[0])
  ```
