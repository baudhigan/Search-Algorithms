# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
### Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
#Developed by: Baudhigan D
#Register number:212223230028
#Program : Linear search
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
array.sort()
k = eval(input()) 
print(array)
res=binarySearchIter(array,k,0,len(array)-1)
if res==-1:
    print("Element not found")
else:
    print("Element found at index: ",res)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binarysearch(array, k, low, high):
    while low <= high:
        mid = low + (high - low)//2
        if array[mid] == k:
            return mid
        elif array[mid] < k:
            low = mid +1
        else:
            high = mid -1
    return -1
array = eval(input())
array.sort()
k = eval(input())
result = binarysearch(array, k, 0, len(array)-1)
if(result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ", result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
def binarysearch(array, k, low, high):
    if low <= high:
        mid = low + (high - low)//2
        if array[mid] == k:
            return mid
        elif array[mid] < k:
            low = mid +1
            return binarysearch(array, k, low, high)
        else:
            high = mid -1
            return binarysearch(array, k, low, high)
    return -1
array = eval(input())
array.sort()
k = eval(input())
result = binarysearch(array, k, 0, len(array)-1)
if(result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ", result)
```
## Sample Input and Output
i)	#Use a linear search method to match the item in a list.
![Screenshot 2024-04-17 100112](https://github.com/baudhigan/Search-Algorithms/assets/151921158/a7b412d4-eb8d-4122-8bfb-ad5fdded6cd7)

ii)	# Find the element in a list using Binary Search(Iterative Method).
![Screenshot 2024-04-17 100213](https://github.com/baudhigan/Search-Algorithms/assets/151921158/fb44d5ea-43d7-4f2c-af52-7c74ec993a44)

iii)	# Find the element in a list using Binary Search (recursive Method).
![Screenshot 2024-04-17 100227](https://github.com/baudhigan/Search-Algorithms/assets/151921158/1eb90b45-33ee-44ee-8e85-0736ee34f67e)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
