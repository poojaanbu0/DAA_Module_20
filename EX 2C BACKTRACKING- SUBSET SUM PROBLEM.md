# EX 2C BACKTRACKING- SUBSET SUM PROBLEM

## AIM:

To demonstrate that the sum of the subset of a given set is equal to the given sum.

## Algorithm:

1.Start with the first number in the list and a running total of 0.

2.At each number, you have two choices:

3.Include the number in the sum.

4.Move to the next number and repeat the process for both choices.

5.Keep doing this until,You reach the end of the list.

6.At that point, check if the current sum equals the target.

7.If you ever reach the target sum, return True (meaning a valid subset was found).

8.If all possibilities are tried and none of them match the target, return False.

9.At the end, print the original list and show whether a valid subset exists.

## Program:

```
# Developed by: Pooja A 
# Register Number:  212222240072

def SubsetSum(a,i,sum,target,n):
    if i == n:
        return sum == target
    
    if SubsetSum(a,i+1,sum+a[i],target,n):   
        return True
        
    if SubsetSum(a,i+1,sum,target,n):   
        return True 
        
    return False    
    
a=[]
size=int(input())
for i in range(size):
    x=int(input())
    a.append(x)

target=int(input())
n=len(a)

if(SubsetSum(a,0,0,target,n)==True):
    for i in range(size):
        print(a[i])
    print("True,subset found")
else:
    for i in range(size):
        print(a[i])
    print("False,subset not found")
```

## Output:
![447225859-b78047f2-3979-40a7-833a-2e077214871e](https://github.com/user-attachments/assets/bf331591-f9b4-4623-8afc-3c50151c4c36)


## Result:
The Subset Sum program executed successfully, and the result was determined based on whether a subset matching the target sum was found or not.
