# Data-Structures-and-Algorithms-Interview
Interview questions on Data structures and algorithms with Python and how to answer them.
## Question 1
1. Write a program to print all the prime numbers in an interval. Given k numbers which are less than n, return the set of prime numbers among them.
```
n = 35 
def solution(n):
    prime_nums = []
    for num in range(n):
        if num > 1: # all prime numbers are greater than 1
            for i in range(2, num):
                if (num % i) == 0: #if the modulus == 0, this means that the number can be  divided by a  number preceeding it
                    break
            else:
                prime_nums.append(num)
    return prime_nums
solution(n)
```
OUTPUT: [2,3,5,7,11,13,17,19,23,29,31]

## Question 2
2. Implement the FizzBuzz algorithm using Python
=> The Fizz and Buzz refers to any number that is a multiple is a multiple of 3 and 5.

Solution:
```
for i in range(1,20):
    if i % 3 == 0 and i % 5 == 0:
        print("FizzBuzz")
    elif i % 3 == 0:
        print("Fizz")
    elif i % 5 == 0:
        print("Buzz")
    else:
        print(i)
        
```
## Question 3
3. Implement Queues in Data structures
=> A queue is a data structure where we insert items from the back and remove items from the front

Solution:
```
class queue:
    def __init__(self):
        self.items = []
    def is_empty(self):
        return self.items == []
    def enqueue(self, item):
        self.items.insert(0, item)
    def dequeue(self):
        return self.items.pop()
    def size(self):
    return len(self.items)
```

## Question 4
4. Implement Linked list in Data structures
=> Linked lists are a sort of data structure in which each data node has a relational pointer that connects it to the next node in the list.

Solution: 
```
class Node:
    def __init__(self, dataval=None):
        self.dataval = dataval
        self.nextval = None 
class SLinkedList:
    def __init__(self):
        self.headval = None
 
list1 = SLinkedList()
list1.headval = Node("Mon")
e2 = Node("Tue")
e3 = Node("Wed")
#Link first Node to second node
list1.headval.nextval = e2
#Link second Node to third node
e2.nextval = e3
```
## Question 5
5. Implement the stack in Data structures and demonstrate the push and pop function
=> A stack is an abstract data type that provides a linear data structure, analogous to a physical stack or pile where objects may only be removed from the top. 
=> As a result, item insertion (push) and deletion (pop) take place only at one end of the stack, the top of the stack, and in a certain order: LIFO (Last In First Out) or FILO (First In Last Out)

Solution: 
```
stack = []
 
#append() function to push element in the stack
stack.append('a')
stack.append('b')
stack.append('c')
 
print('Initial stack')
print(stack)
 
#pop() function to pop element from stack in LIFO order
print('\nElements popped from stack:')
print(stack.pop())
print(stack.pop())
print(stack.pop())
 
print('\nStack after elements are popped:')
print(stack)
 
#uncommenting print(stack.pop()) will cause an IndexError as the stack is now empty
```
