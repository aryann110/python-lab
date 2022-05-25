# python-lab
This reporsitory is of python programming lab submitted to Manoj Varshney sir by Aryan Dahiya B.Tech Sec-l ROLL NO.-2115000212

Ques1 -  Write a program to check wether the number is neon or not
num=int(input("enter the number:"))
temp=num*num
sum=0
while(temp>0):
    rem=temp%10
    sum=sum+rem
    temp=temp//10
if(sum==num):
    print("the number is neon number!")
else:
    print("the number is not a neon number!")
    
Ques2 - to print an table of a number
num=int(input("enter the number:"))
i=1
while(i<=10):
    print("%d   X   %d  =   %d"%(i,num,i*num))
    i+=1
 
Ques3 - enter the mobile number and print the of odd digit index
num=int(input("enter the 10 digit number:"))
i=10
sumodd=0
sumeven=0
while(i>=0):
    if(i%2==0):
        rem=num%10
        sumodd=sumodd+rem
        num=num//10
        i-=1
    else:
        rem=num%10
        sumeven=sumeven+rem
        num=num//10
        i-=1 
if(sumodd==sumeven):
    print("magic")
else:
    print("not")
    
Ques 4 - write a program check wether it is armstrong or not
import math
num=int(input("enter the number:"))
temp=num
sum=0
dig=math.log10(num)+1
print(dig)
while(num>0):
    rem=num%10
    sum=sum+(rem**int(dig))
    print(sum,rem)
    num=num//10
if(sum==temp):
    print("armstrong")
else:
    print("not")
    
Ques5 - write a program to check perfect or not
num=int(input("Enter the number: "))  
sum_v=0  
for i in range(1,num):  
    if (num%i==0):  
        sum_v=sum_v+i  
if(sum_v==num):  
    print("The entered number is a perfect number")  
else:  
    print("The entered number is not a perfect number")  
    
Ques6 - enter a no from user and print its table.
num=int(input())
lst=[]
for i in range(1,11):
    lst.append(i)
lst1=list(map(lambda n1:n1*num,lst))
print(lst1)

Ques7 - print list in which all number is greater then 18
lst=[]
lst=list(map(int,input().split()))
lst1=list(filter(lambda n:n>=18,lst))
print(lst1)"""
#question3====>upper case swap list
"""lst=list(map(str,input().split()))
lst1=list(map(lambda n:n.upper(),lst))
print(lst1)

Qeus8 - write a program to print the fibonacci series
n=int(input())
lst=[0,1]
lst1=list(map(lambda n:lst.append(lst[-1]+lst[-2]),range(n-2)))
print(lst)

Ques9 - enter two list from user and then print a third list having common element of those list
lst1=list(map(int,input().split()))
lst4=[]
for i in lst1:
    if i not in lst4:
        lst4.append(i)
lst2=list(map(int,input().split()))
lst5=[]
for i in lst2:
    if i not in lst5:
        lst5.append(i)
lst3=list(filter(lambda n: n in lst1,lst2))
print(lst3)

Ques10 - enter a list from user and check even and off elements in it
lst=list(map(int,input().split()))
lst1=list(filter(lambda n:n%2==0,lst))
print('even number',len(lst1))
lst2=list(filter(lambda n:n%2!=0,lst))
print('odd number',len(lst2)

Ques11 - enter a list and write it in upper case
lst=list(map(str,input().split()))
lst1=list(map(lambda n:n.upper(),lst))
print(lst1)

Ques13 - enter a dictionary from user and find the sum of values.
dict={}
size=int(input("enter the size of the dict:"))
for i in range (size):
    keys=input()
    values=int(input())
    dict.update({keys:values})
print(dict)
print("sum of all the values is:",end='')
print(sum(dict.values()))

Ques14 - enter a dictionary from user and sort the values into a list
dict={}
size=int(input("enter the size of the dict:"))
for i in range (size):
    keys=int(input())
    values=int(input())
    dict.update({keys:values})
print(dict)
print(sorted(dict.values()))

Ques15 - enter two dictionary from user and merge them into third dictionary
dict={}
size=int(input("enter the size of the dict:"))
for i in range (size):
    keys=int(input())
    values=int(input())
    dict.update({keys:values})
print(dict)
dict1={}
size=int(input("enter the size of the dict:"))
for i in range (size):
    keys=int(input())
    values=int(input())
    dict1.update({keys:values})
print(dict1)

dict2={}
for i in (dict,dict1):
    dict2.update(i)
print(dict2)

Ques16 - enter a dictionary from user and find the sum of values using for loop
ict={}
size=int(input("enter the size of the dict:"))
for i in range (size):
    keys=int(input())
    values=int(input())
    dict.update({keys:values})
print(dict)
sum=0
for i in dict.values():
    sum=sum+i
print(sum)

Ques17 - check wether the key is present in the dict or not
         #if present then print its value else print
         #key not found
 dict={}
size=int(input("enter the size of the dict:"))
for i in range (size):
    keys=int(input())
    values=int(input())
    dict.update({keys:values})
print(dict)
check=int(input("enter the key which u want to check:"))
if check in dict.keys():
    print(dict[check])
else:
    print("key not found!")
    
Ques18 - enter a dictionary from user and print the multiplicayion of all keys and values
dict={}
size=int(input("enter the size of the dict:"))
for i in range (size):
    keys=int(input())
    values=int(input())
    dict.update({keys:values})
print(dict)

Ques19 - enter a file with data and copy odd number of lines into another file
f=open('aryan.txt','r')
f1=open("a.txt","w+")
str=f.readlines()
print(str)
for i in range(len(str)):
    if i%2==0:
        print(str[i])
        f1.write(str[i])
        f1.write("\n")
f1.seek(0,0)
a=f1.read()
print(a)
f1.close()
f.close()

Ques20 - in a file copy odd no, of words
f=open('aryan.txt','r')
f1=open('a.txt','w+')
str=f.read().split()
print(str)
for i in range(len(str)):
    if i%2==0:
       print(str[i])
       f1.write(str[i])
       f1.write(' ')
f1.seek(0,0)
a=f1.read()
print(a)
f1.close()
f.close()

Ques21 - in a file count number of spaces and tabs
f=open('aryan.txt','r')
s=n=t=0
str=f.read()
for i in str:
    if ord(i)==32:
        s+=1
    elif i=='\n':
        n+=1
    elif i=='\t':
        t+=1
print(s,n,t)
f.close()

Ques22 - count total number of lines in a file
f=open('aryan.txt','r')
f.seek(0,0)
sum=0
str=f.read()
print(str)
for i in str:
    if i=='\n':
        sum+=1
print(sum)
f.close()

Ques23 - count total number of words in a file
f=open('aryan.txt','r')
f.seek(0,0)
sum=0
str=f.read()
a=str.split()
print(a,type(a))
for i in a:
    sum+=1
print(sum)
f.close()

Ques24 - in a file count total number of characters
f=open('aryan.txt','r')

sum=0
str=f.read()
f.seek(0,0)
for i in str:
    sum+=1
print(sum-1)
f.close()

Ques25 - in a file count number of to and the
f=open('aryan.txt','r')
f.seek(0,0)
str=f.read()
print(str)
b=str.lower()
print(b)
b=b.split()
print(b)
sum=0
for i in b:
    if i =='to' or i=='and' or i=='the':
            sum+=1
print(sum)
f.close()

Ques26 - write a program to read lines in a file
f=open('aryan.txt','r')
str=f.readlines()
print(str,type(str))
f.close()

Ques27 - 
