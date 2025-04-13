# python-programs
def odd_even(num):
    if num%2==0:
        return "even"
    else:  
        return "odd"
def prime(num):
    if num<=2:
        return False
    for i in range(2,num):
        if num%i==0:
            return False
    return True
def fact(num):
    if num==0:
        return "1"
    else:
        x=1
        for i in range(1,num+1):
            x *= i
        return x
def factR(num):
    if num==0:
        return 1
    else:
        return num*factR(num-1)
def reverse(num):
    reverse=0
    while num!=0:
        digit=num%10
        reverse=reverse*10+digit
        num=num//10
    return reverse
def count(num):
    count=0
    if num==0:
        return 1
    else:
        while num!=0:
            num = num//10
            count+=1
        return count
name= input("Enter the name: ")
age = int(input("Enter the age: "))
print(f"Hello {name}, Welcome to Number anlyzer:")
n = int(input("Enter the number:"))
print(f"{n} is {odd_even(n)}")
if prime(n):
    print(f"{n} is prime number")
else:
    print(f"{n} is not prime number")
    
print(f"The factorial of {n} is {fact(n)} through loop")
print(f"The factorial of {n} is {factR(n)} through resursion")
print(f"Reverse number is {reverse(n)}")
print(f"The total number of digits is {count(n)}")
