# 🆂🆄🅳🅾🅺🆄-🆆🅸🆃🅷-🅿🆈🆃🅷🅾🅽
<img src="https://user-images.githubusercontent.com/76767487/148503349-9bd708ba-e619-4f22-8214-518a988a5271.png" width="50" height="50">



### 𝐰𝐞𝐥𝐜𝐨𝐦𝐞 𝐛𝐚𝐜𝐤 , 𝐈𝐧 𝐭𝐡𝐢𝐬 𝐫𝐞𝐩𝐨𝐬𝐢𝐭𝐨𝐫𝐲 𝐰𝐞 𝐰𝐢𝐥𝐥 𝐥𝐞𝐚𝐫𝐧 𝐭𝐨 𝐦𝐚𝐤𝐞 𝐬𝐮𝐝𝐨𝐤𝐮 𝐬𝐨𝐥𝐯𝐞𝐫 .  

𝐑𝐞𝐪𝐮𝐢𝐫𝐞𝐦𝐞𝐧𝐭𝐬 :->  𝐁𝐚𝐬𝐢𝐜 𝐤𝐧𝐨𝐰𝐥𝐞𝐝𝐠𝐞 𝐚𝐛𝐨𝐮𝐭 𝐬𝐮𝐝𝐨𝐤𝐮 , 𝐦𝐚𝐭𝐫𝐢𝐱 , 𝐟𝐮𝐧𝐜𝐭𝐢𝐨𝐧𝐬 .


we need a matrix to test our code 's output . 
```yml
import numpy as np

matrix =np.array([[1,0,0,4,8,9,0,0,6],
                  [7,3,0,0,0,0,0,4,0],
                  [0,0,0,0,0,1,2,9,5],
                  [0,0,7,1,2,0,6,0,0],
                  [5,0,0,7,0,3,0,0,8],
                  [0,0,6,0,9,5,7,0,0],
                  [9,1,4,6,0,0,0,0,0],
                  [0,2,0,0,0,0,0,3,7],
                  [8,0,0,5,1,2,0,0,4]])
```

Now we will create a function named solve , In which requires matrix as arguments .
```yml
def solve(matrix):
    import copy
    matrixs = copy.copy(matrix)
    x=[]
    for o in range(len(matrix)):
        for oo in range(len(matrix[o])):
            if matrix[o][oo] == 0:
                x.append((o,oo))
    rows=0
    cols=0
                 
```
here we have first make empty list  , and store the location in that list whose element is 0 in matrix .
 
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
after rows=0 and cols=0 we continue , now in first for loop we are getting one by one position of the empty element . And make the instance of i which will help in backpropagates . we define a function which we helps us call inside just like recurssion function  . first we get the value which will be initially zero ,in part 1 checking we make a for loop and search a number from 1 to 9 which in not in that row and columns , if that number is in that row or column we will make exits =1 , and if num is in row or col and num = 9 , it will make exits =2 , if number is not in row or col , it will not make any diffrence to exits which is intially zero. 
In part 2 checking we will chech whether the number is in that 3 x 3 box or not same as previous one , if num is in box make exits =1  , if num is in box and having value 9 it will make exits = 2.
```yml
rows=0
cols=0

for i in range(len(x)):
                copy_i=i
                rows=x[i][0]
                cols=x[i][1]
                def function(x,rows,cols,matrix,i,copy_i):
                    g = matrix[rows][cols]
                    
                    for k in range(g+1,10):
                        #------------------ part 1 checking
                        exits=0
                        for l in range(len(matrix)):
                            if matrix[rows][l] == k and k == 9 or matrix[l][cols] == k and k == 9:
                                exits=2
                                break
                            elif matrix[rows][l] == k or matrix[l][cols] == k:
                                exits=1
                                break
                        #------------------ part 2 checking
                        ro = copy.copy(rows)//3
                        col = copy.copy(cols) //3
                        for b in range(3):
                            for n in range(3):
                                if matrix[ro*3:ro*3+3,col*3:col*3+3][b][n]==k and k==9:
                                  exits=2
                                  break
                                elif matrix[ro*3:ro*3+3,col*3:col*3+3][b][n] == k :
                                  exits=1
                                  break
```


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
```yml
import numpy as np

matrix =np.array([[1,0,0,4,8,9,0,0,6],
                  [7,3,0,0,0,0,0,4,0],
                  [0,0,0,0,0,1,2,9,5],
                  [0,0,7,1,2,0,6,0,0],
                  [5,0,0,7,0,3,0,0,8],
                  [0,0,6,0,9,5,7,0,0],
                  [9,1,4,6,0,0,0,0,0],
                  [0,2,0,0,0,0,0,3,7],
                  [8,0,0,5,1,2,0,0,4]])




def solve(matrix):
    import copy
    matrixs = copy.copy(matrix)
    x=[]
    for o in range(len(matrix)):
        for oo in range(len(matrix[o])):
            if matrix[o][oo] == 0:
                x.append((o,oo))
    rows=0
    cols=0
 
    for i in range(len(x)):
                ww=i
                rows=x[i][0]
                cols=x[i][1]
                def function(x,rows,cols,matrix,i,ww):
                    g = matrix[rows][cols]
                    if g==9:
                        matrix[rows][cols]=0
                        i= i-1
                        rows=x[i][0]
                        cols=x[i][1]
                        matrix,i = function(x,rows,cols,matrix,i,ww) 
                    for k in range(g+1,10):
                        exits=0
                        for l in range(len(matrix)):
                            if matrix[rows][l] == k and k == 9 or matrix[l][cols] == k and k == 9:
                                exits=2
                                break
                            elif matrix[rows][l] == k or matrix[l][cols] == k:
                                exits=1
                                break
                            
                        ro = copy.copy(rows)//3
                        col = copy.copy(cols) //3
                        for b in range(3):
                            for n in range(3):
                                if matrix[ro*3:ro*3+3,col*3:col*3+3][b][n]==k and k==9:
                                  exits=2
                                  break
                                elif matrix[ro*3:ro*3+3,col*3:col*3+3][b][n] == k :
                                  exits=1
                                  break
                       
                        if exits==0:
                            matrix[x[i][0]][x[i][1]]=k  
                            if ww!=i:
                                i+=1
                                rows=x[i][0]
                                cols=x[i][1]
                                matrix,i = function(x,rows,cols,matrix,i,ww)
                            break   
                        elif exits==2:
                            matrix[rows][cols]=0
                            i= i-1
                            rows=x[i][0]
                            cols=x[i][1] 
                            matrix,i = function(x,rows,cols,matrix,i,ww)
                    return matrix,i   
                matrix,i = function(x,rows,cols,matrix,i,ww)              
    return matrix,matrixs


def print_matrix(matrix):
    
    for i in range(1,10):
        for j in range(1,10):
            if j==1:
                print("|",end="") 
            print(matrix[i-1,j-1]," ",end="")
            if j%3==0:
                print("|",end="")      
        print("")
        if i%3==0:
            print("-------------------------------")
                
    
    
solved,que = solve(matrix)
print("Question is  :\n")
print_matrix(que)    
print("\nAnswer is :\n")
print_matrix(solved)

```


