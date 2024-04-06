## Developed by: HARISH S
## RegisterNumber:212223230071

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
#Developed by: HARISH S
#RegisterNumber:212223230071
def l(arr,b):
    for i in range(len(arr)):
        if arr[i]==b:
            return i
    return -1
arr=eval(input())
b=int(input())
arr.sort()
print(arr)
result=l(arr,b)
if result!=-1:
    print("Element found at index: ",result)
else:
    print("Element not found")
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
#  Binary Search(Iterative Method).
# Developed by: HARISH S
# RegisterNumber:212223230071
def binary_search(arr, target):
    left, right = 0, len(arr) - 1

    while left <= right:
        mid = (left + right) 
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1

arr = eval(input())
target = int(input())
arr.sort()
print(arr)
result = binary_search(sorted(arr), target)

if result != -1:
    print("Element found at index: ", result)
else:
    print("Element not found")
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
# Binary Search (recursive Method).
# Developed by: HARISH S
# RegisterNumber:212223230071
def binary_search_recursive(arr, target, left, right):
    if left <= right:
        mid = (left + right) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            return binary_search_recursive(arr, target, mid + 1, right)
        else:
            return binary_search_recursive(arr, target, left, mid - 1)
    return -1

arr = eval(input())
target = int(input())
arr.sort()
print(arr)
result = binary_search_recursive(arr, target, 0, len(arr) - 1)
if result != -1:
    print("Element found at index: ", result)
else:
    print("Element not found")

```
## Sample Input and Output

![image](https://github.com/pirateharishs/Search-Algorithms/assets/166011385/61526866-23b8-467f-b4b7-20c38b6c336e)

![image](https://github.com/pirateharishs/Search-Algorithms/assets/166011385/6d997c1a-d7fb-45d6-9f3f-23d9516feb43)

![image](https://github.com/pirateharishs/Search-Algorithms/assets/166011385/2b36afbd-029f-4d4a-aa4b-850732b39fe9)

![image](https://github.com/pirateharishs/Search-Algorithms/assets/166011385/340f3065-ee6e-446d-ba43-c0275ad0f4a6)

![image](https://github.com/pirateharishs/Search-Algorithms/assets/166011385/e60a4f97-8870-404b-8d58-5fd11b61015a)


![image](https://github.com/pirateharishs/Search-Algorithms/assets/166011385/35f61715-5383-40b0-a846-cc19ce016691)





## Result
Thus the linear search and binary search algorithm is implemented using python programming.
