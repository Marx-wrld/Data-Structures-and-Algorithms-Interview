# Data-Structures-and-Algorithms-Interview
Interview questions on Data structures and algorithms with Python and how to answer them.
## Question 1
1. Write a program to print all the prime numbers in an interval. Given k numbers which are less than n, return the set of prime numbers among them.

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

OUTPUT: [2,3,5,7,11,13,17,19,23,29,31]

## Question 2
2. Implement the FizzBuzz algorithm using Python
=> The Fizz and Buzz refer to any number that is a multiple is a multiple of 3 and 5.

Solution:

  for i in range(1,20):
    if i % 3 == 0 and i % 5 == 0:
        print("FizzBuzz")
    elif i % 3 == 0:
        print("Fizz")
    elif i % 5 == 0:
        print("Buzz")
    else:
        print(i)
        
## Question 3

