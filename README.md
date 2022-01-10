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
𝐚𝐟𝐭𝐞𝐫 𝐫𝐨𝐰𝐬=𝟎 𝐚𝐧𝐝 𝐜𝐨𝐥𝐬=𝟎 𝐰𝐞 𝐜𝐨𝐧𝐭𝐢𝐧𝐮𝐞 , 𝐧𝐨𝐰 𝐢𝐧 𝐟𝐢𝐫𝐬𝐭 𝐟𝐨𝐫 𝐥𝐨𝐨𝐩 𝐰𝐞 𝐚𝐫𝐞 𝐠𝐞𝐭𝐭𝐢𝐧𝐠 𝐨𝐧𝐞 𝐛𝐲 𝐨𝐧𝐞 𝐩𝐨𝐬𝐢𝐭𝐢𝐨𝐧 𝐨𝐟 𝐭𝐡𝐞 𝐞𝐦𝐩𝐭𝐲 𝐞𝐥𝐞𝐦𝐞𝐧𝐭 . 𝐀𝐧𝐝 𝐦𝐚𝐤𝐞 𝐭𝐡𝐞 𝐢𝐧𝐬𝐭𝐚𝐧𝐜𝐞 𝐨𝐟 𝐢 𝐰𝐡𝐢𝐜𝐡 𝐰𝐢𝐥𝐥 𝐡𝐞𝐥𝐩 𝐢𝐧 𝐛𝐚𝐜𝐤𝐩𝐫𝐨𝐩𝐚𝐠𝐚𝐭𝐞𝐬 . 𝐰𝐞 𝐝𝐞𝐟𝐢𝐧𝐞 𝐚 𝐟𝐮𝐧𝐜𝐭𝐢𝐨𝐧 𝐰𝐡𝐢𝐜𝐡 𝐰𝐞 𝐡𝐞𝐥𝐩𝐬 𝐮𝐬 𝐜𝐚𝐥𝐥 𝐢𝐧𝐬𝐢𝐝𝐞 𝐣𝐮𝐬𝐭 𝐥𝐢𝐤𝐞 𝐫𝐞𝐜𝐮𝐫𝐬𝐬𝐢𝐨𝐧 𝐟𝐮𝐧𝐜𝐭𝐢𝐨𝐧  . 𝐟𝐢𝐫𝐬𝐭 𝐰𝐞 𝐠𝐞𝐭 𝐭𝐡𝐞 𝐯𝐚𝐥𝐮𝐞 𝐰𝐡𝐢𝐜𝐡 𝐰𝐢𝐥𝐥 𝐛𝐞 𝐢𝐧𝐢𝐭𝐢𝐚𝐥𝐥𝐲 𝐳𝐞𝐫𝐨 ,𝐢𝐧 𝐩𝐚𝐫𝐭 𝟏 𝐜𝐡𝐞𝐜𝐤𝐢𝐧𝐠 𝐰𝐞 𝐦𝐚𝐤𝐞 𝐚 𝐟𝐨𝐫 𝐥𝐨𝐨𝐩 𝐚𝐧𝐝 𝐬𝐞𝐚𝐫𝐜𝐡 𝐚 𝐧𝐮𝐦𝐛𝐞𝐫 𝐟𝐫𝐨𝐦 𝟏 𝐭𝐨 𝟗 𝐰𝐡𝐢𝐜𝐡 𝐢𝐧 𝐧𝐨𝐭 𝐢𝐧 𝐭𝐡𝐚𝐭 𝐫𝐨𝐰 𝐚𝐧𝐝 𝐜𝐨𝐥𝐮𝐦𝐧𝐬 , 𝐢𝐟 𝐭𝐡𝐚𝐭 𝐧𝐮𝐦𝐛𝐞𝐫 𝐢𝐬 𝐢𝐧 𝐭𝐡𝐚𝐭 𝐫𝐨𝐰 𝐨𝐫 𝐜𝐨𝐥𝐮𝐦𝐧 𝐰𝐞 𝐰𝐢𝐥𝐥 𝐦𝐚𝐤𝐞 𝐞𝐱𝐢𝐭𝐬 =𝟏 , 𝐚𝐧𝐝 𝐢𝐟 𝐧𝐮𝐦 𝐢𝐬 𝐢𝐧 𝐫𝐨𝐰 𝐨𝐫 𝐜𝐨𝐥 𝐚𝐧𝐝 𝐧𝐮𝐦 = 𝟗 , 𝐢𝐭 𝐰𝐢𝐥𝐥 𝐦𝐚𝐤𝐞 𝐞𝐱𝐢𝐭𝐬 =𝟐 , 𝐢𝐟 𝐧𝐮𝐦𝐛𝐞𝐫 𝐢𝐬 𝐧𝐨𝐭 𝐢𝐧 𝐫𝐨𝐰 𝐨𝐫 𝐜𝐨𝐥 , 𝐢𝐭 𝐰𝐢𝐥𝐥 𝐧𝐨𝐭 𝐦𝐚𝐤𝐞 𝐚𝐧𝐲 𝐝𝐢𝐟𝐟𝐫𝐞𝐧𝐜𝐞 𝐭𝐨 𝐞𝐱𝐢𝐭𝐬 𝐰𝐡𝐢𝐜𝐡 𝐢𝐬 𝐢𝐧𝐭𝐢𝐚𝐥𝐥𝐲 𝐳𝐞𝐫𝐨. 
𝐈𝐧 𝐩𝐚𝐫𝐭 𝟐 𝐜𝐡𝐞𝐜𝐤𝐢𝐧𝐠 𝐰𝐞 𝐰𝐢𝐥𝐥 𝐜𝐡𝐞𝐜𝐡 𝐰𝐡𝐞𝐭𝐡𝐞𝐫 𝐭𝐡𝐞 𝐧𝐮𝐦𝐛𝐞𝐫 𝐢𝐬 𝐢𝐧 𝐭𝐡𝐚𝐭 𝟑 𝐱 𝟑 𝐛𝐨𝐱 𝐨𝐫 𝐧𝐨𝐭 𝐬𝐚𝐦𝐞 𝐚𝐬 𝐩𝐫𝐞𝐯𝐢𝐨𝐮𝐬 𝐨𝐧𝐞 , 𝐢𝐟 𝐧𝐮𝐦 𝐢𝐬 𝐢𝐧 𝐛𝐨𝐱 𝐦𝐚𝐤𝐞 𝐞𝐱𝐢𝐭𝐬 =𝟏  , 𝐢𝐟 𝐧𝐮𝐦 𝐢𝐬 𝐢𝐧 𝐛𝐨𝐱 𝐚𝐧𝐝 𝐡𝐚𝐯𝐢𝐧𝐠 𝐯𝐚𝐥𝐮𝐞 𝟗 𝐢𝐭 𝐰𝐢𝐥𝐥 𝐦𝐚𝐤𝐞 𝐞𝐱𝐢𝐭𝐬 = 𝟐.

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
                                  
                    return matrix,i

```

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Now we have add before checking a if condition for backpropagation  if the number is already 9 than we will again backpropagate a layer by decrement i - 1 and call function again . due to call the function again it will update the previos element .

```yml
rows=0
cols=0

for i in range(len(x)):
                copy_i=i
                rows=x[i][0]
                cols=x[i][1]
                
                def function(x,rows,cols,matrix,i,copy_i):
                    g = matrix[rows][cols]
                    if g==9:
                        matrix[rows][cols]=0
                        i= i-1
                        rows=x[i][0]
                        cols=x[i][1]
                        matrix,i = function(x,rows,cols,matrix,i,copy_i)
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

                    return matrix,i

```

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Now after checking if exits = 0 means number is not in box or row or col that means we can put the value in that empty space after that copy_i != i 

```yml
rows=0
cols=0

for i in range(len(x)):
                copy_i=i
                rows=x[i][0]
                cols=x[i][1]
                
                def function(x,rows,cols,matrix,i,copy_i):
                    g = matrix[rows][cols]
                    if g==9:
                        matrix[rows][cols]=0
                        i= i-1
                        rows=x[i][0]
                        cols=x[i][1]
                        matrix,i = function(x,rows,cols,matrix,i,copy_i)
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
                        
                        if exits==0:
                            matrix[x[i][0]][x[i][1]]=k  
                            if copy_i!=i:
                                i+=1
                                rows=x[i][0]
                                cols=x[i][1]
                                matrix,i = function(x,rows,cols,matrix,i,copy_i)
                            break   
                        elif exits==2:
                            matrix[rows][cols]=0
                            i= i-1
                            rows=x[i][0]
                            cols=x[i][1] 
                            matrix,i = function(x,rows,cols,matrix,i,copy_i)
                    return matrix,i

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


