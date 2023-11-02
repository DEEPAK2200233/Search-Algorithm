# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by: DEEPAK RAJ S
RegisterNumber: 212222240023
'''
def linearSearch(array,k):
    for i in array:
        if i==k:
            return array.index(i)
    return -1
array = eval(input())
k = eval(input())
array.sort()
print(array)
result = linearSearch(array,k)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: DEEPAK RAJ S
RegisterNumber: 212222240023
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array = eval(input())
k = eval(input())
array.sort()
print(array)
result=binarySearchIter(array, k,0,len(array)-1)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: DEEPAK RAJ S
RegisterNumber: 212222240023
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            return binarySearchIter(array, k, mid+1, high)
        else:
            return binarySearchIter(array, k, low, mid-1)
    return -1
array = eval(input())
k = eval(input())
array.sort()
print(array)
result=binarySearchIter(array, k,0,len(array)-1)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)
```
## Sample Input and Output
i)	#Use a linear search method to match the item in a list.
![WhatsApp Image 2023-11-02 at 15 33 16_4b5c55b5](https://github.com/DEEPAK2200233/Search-Algorithm/assets/118707676/0c2f320d-c1dc-47c7-a8c0-91d77c76c0cf)
ii)	# Find the element in a list using Binary Search(Iterative Method).
![WhatsApp Image 2023-11-02 at 15 34 24_440909f8](https://github.com/DEEPAK2200233/Search-Algorithm/assets/118707676/daa929eb-415c-4c92-b930-061e8d7962f4)
iii)	# Find the element in a list using Binary Search (recursive Method).
![image](https://github.com/DEEPAK2200233/Search-Algorithm/assets/118707676/6b9d4004-d57e-447a-86e4-65bd20f71692)
## Result
Thus the linear search and binary search algorithm is implemented using python programming.
