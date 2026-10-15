Name- MOHD AAHIL <BR>
ID- MCAI2026038 <BR>
ROLL NO. 2620235022 <BR>
MENTOR- AKHILESH MISHRA <BR>
ABOUT- DAILY CLASS WORK, IN WHICH WE PRACTICE PYTHON.


```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```


```python
 #list Data Type
data =[] #empty list
data =[10,20,30,40,50]
print("Before change: " ,data[3])

data[3]=60 #List is mutable
print("After change: ",data[3])

print (data[-1]) #Last Element
```

    Before change:  40
    After change:  60
    50
    


```python
studentRecord =["Soniya",23,"Java", 20000.00, True] #hetrogeneous type
print(studentRecord[0]) #indexing
print(studentRecord[0:3]) #slicing
```

    Soniya
    ['Soniya', 23, 'Java']
    


```python
studentNames=["Zayn","Zatch","Eren","Mikasa","Levi","Arwin"] #Duplicate Elements
print(studentNames[0])
print(studentNames[0:3])
print(studentNames[:]) #print entire list
print(studentNames) #print entire list
```

    Zayn
    ['Zayn', 'Zatch', 'Eren']
    ['Zayn', 'Zatch', 'Eren', 'Mikasa', 'Levi', 'Arwin']
    ['Zayn', 'Zatch', 'Eren', 'Mikasa', 'Levi', 'Arwin']
    


```python
#Methods of list
studentNames=["Zayn","Zatch","Eren","Mikasa","Levi","Arwin"] #Duplicate Elements
#Len()
print(len(studentNames))

#append()
studentNames.append("Armin")
print(studentNames)

#insert()
studentNames.insert(0,"Historia")
print(studentNames)
```

    6
    ['Zayn', 'Zatch', 'Eren', 'Mikasa', 'Levi', 'Arwin', 'Armin']
    ['Historia', 'Zayn', 'Zatch', 'Eren', 'Mikasa', 'Levi', 'Arwin', 'Armin']
    


```python
#Methods of list
studentNames=["Zayn","Zatch","Eren","Mikasa","Levi","Arwin"]
studentNames.extend(["Luffy","Zoro"])
print(studentNames)

#remove()
studentNames.remove("Zoro")
print(studentNames)

studentNames.remove("Luffy") #valueError: List.remove(x): x not in list
studentNames.pop(1)
```

    ['Zayn', 'Zatch', 'Eren', 'Mikasa', 'Levi', 'Arwin', 'Luffy', 'Zoro']
    ['Zayn', 'Zatch', 'Eren', 'Mikasa', 'Levi', 'Arwin', 'Luffy']
    




    'Zatch'




```python
#Methods of list
studentNames=["Zayn","Zatch","Eren","Mikasa","Levi","Arwin"]
print(studentNames.pop())
print(studentNames.pop(1))
print(studentNames)
3studentNames.pop(10) #IndexError: pop indexout of range
```

    Arwin
    Zatch
    ['Zayn', 'Eren', 'Mikasa', 'Levi']
    


    ---------------------------------------------------------------------------

    IndexError                                Traceback (most recent call last)

    Cell In[12], line 6
          4 print(studentNames.pop(1))
          5 print(studentNames)
    ----> 6 studentNames.pop(10) #IndexError: pop indexout of range
    

    IndexError: pop index out of range



```python
#Methods of list
studentNames=["Zayn","Zatch","Eren","Mikasa","Levi","Arwin"]
studentNames.clear()

print(studentNames)
```

    []
    


```python
#Methods of list
studentNames=["Zayn","Zatch","Eren","Zayn","Levi","Arwin"]
print(studentNames.index("Zayn"))
print(studentNames.index("Zayn",2))
```

    0
    3
    


```python
#Methods of list
studentNames=["Zayn","Zatch","Eren","Zayn","Levi","Arwin"]
print(studentNames.count("Zayn"))
```

    2
    


```python
data=[54,65,34,45,20,78]
data.sort()
print(data)

data.sort(reverse=True)
print(data)
```

    [20, 34, 45, 54, 65, 78]
    [78, 65, 54, 45, 34, 20]
    


```python
data=[54,65,34,45,20,78]
data.reverse()
print(data)
```

    [78, 20, 45, 34, 65, 54]
    


```python
data=[54,65,34,45,20,78]
newdata=data.copy()
print(newdata)
```

    [54, 65, 34, 45, 20, 78]
    


```python
data=[54,65,34,45,20,78]
a=data
print(a)
print(type(a))
```

    [54, 65, 34, 45, 20, 78]
    <class 'list'>
    


```python
#Tuple
    #Important Point: Parentheses () are commonly used to create tuples
data={10,20,30,40,50}
print(type(data))
```

    <class 'set'>
    


```python
# But Parentheses are not actually mandatory
# The  comma, is what makes a tuple, not the parentheses.
data2=10,20,30,40,50
print(type(data2))
```

    <class 'tuple'>
    


```python
data3=(10)
print(type(data3))
#Output: <class 'int'>

# why?
# Because (10) is not a tuple. It is simply an integer 10 enclosed in parentheses.

#Python treats it as:
# data3 = 10
```

    <class 'int'>
    


```python
#How to create a single-element tuple?
#You must use a comma:
data4=(10,)
print(type(data4))

#Remember this rule:
#Code Type
# data = (10)        int
# data = (10,)       tuple
# data = 10,         tuple
# data = (10, 20)    tuple
```

    <class 'tuple'>
    


```python
#Tuple Indexing
#Tuple are ordered and immutable.
data=(10,20,30,40,50)
print(data[2]) #Indexing is used to access individual elements of a tuple and Tuple indexing starts from 0.
print(data[-1]) #Negative indexing starts from -1 from the right side.
```

    30
    50
    


```python
#A tuple allows duplicate elements.
data=(10,20,30,40,50,30) #Duplicate Elements
print(data)
```

    (10, 20, 30, 40, 50, 30)
    


```python
#Tuple is immutable
#A tuple is immuatable, which means its elements cannot be changed, updated, or deleted after creation.
data=(10,20,30,40,50)
data[0]=88 #tries to change the first element from 10nto 88. Therefore, Python raises a TypeError.

#TypeError: 'tuple' object does not support item assignment
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[10], line 4
          1 #Tuple is immutable
          2 #A tuple is immuatable, which means its elements cannot be changed, updated, or deleted after creation.
          3 data=(10,20,30,40,50)
    ----> 4 data[0]=88 #tries to change the first element from 10nto 88. Therefore, Python raises a TypeError.
          6 #TypeError: 'tuple' object does not support item assignment
    

    TypeError: 'tuple' object does not support item assignment



```python
#Tuple Packing:
studentData="Zayn","MCA AI", 92.65 # Tuple Packing: Tuple Packing Means storing multiple values into a single tuple without explicitly using parentheses.
print(type(studentData))

#Tuple Unpacking
name,course,avgMarks=studentData #Tuple Unpacking means extracting the elements of a tuple into seprate variables.
print(name)
#Note: The number of variable should normally match the number of tuple elements.
```

    <class 'tuple'>
    Zayn
    


```python
record="Zatch","MCA",23,True #Tuple Packing
print(record[0])
print(record[1])
print(record)

name,course,age,att=record
#name,course,age,att="Zatch","MCA",23,True |Tuple Unpacking

print(name)

#Unpacking Using
# * in tuple unpacking is called extended unpacking. It allows one variable to collect multiple remaining values.
n,*ab=record
# Note: The * Operator collects the remaining elements into a list.
print(n)
print(ab)
```

    Zatch
    MCA
    ('Zatch', 'MCA', 23, True)
    Zatch
    Zatch
    ['MCA', 23, True]
    


```python
record="Zatch","MCA",23,True #Tuple Packing
name,course,age=record #ValueError: too many values to unpack (expected 3)
#Note: The number of variables should normally natch the number of tuple elements.  
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    Cell In[16], line 2
          1 record="Zatch","MCA",23,True #Tuple Packing
    ----> 2 name,course,age=record
    

    ValueError: too many values to unpack (expected 3)



```python
record="Zatch","MCA",23,True #Tuple Packing
name,*ab,att=record
print(name)
print(ab)
print(att)
```

    Zatch
    ['MCA', 23]
    True
    


```python
#len() Returns the total number of elements
data=(10,20,30,40,50,30)
print(len(data))

#count() : Counts how many times a value occurs
print(data.count(30))

print(sum(data)) #Returns the sum of numeric elements
print(max(data)) #Retuens the largest element
print(min(data)) #Returns the smallest element
print(data.index(10)) #Returns the index of the first occurrence
```

    6
    2
    180
    50
    10
    0
    


```python
x,y=10,20
print(x+y)
print(x-y)
print(x*y)
print(x/y)

#floor division
print(7//2) #3 Floor division returns the floor value (greatest integer less than or equal to the result).
print(-7//2) #-4
print(2**3) #8 Exponentiation ** is used to calculate the power of a number.
#Important Note: Floor division does not simply remove the decimal part; it moves the result toward negative infinity. 
```

    30
    -10
    200
    0.5
    3
    -4
    8
    


```python
firstName="Zayn"
lastName="Zaidi"
print(firstName+lastName)
```

    ZaynZaidi
    


```python
#Compound Assignment Operators: Compound assignment operators are used to perform an operation and assign the result back to the same variable.

x,y=40,50
x+=y #x=x+y >>>    x=40+50     >>>x=90
print(x)

x-=y #x=x-y >>>    x=90-50     >>>x=40
print(x)

x*=y #x=x*y >>>    x=40*50     >>>x=2000
print(x)

x/=y #x=x/y >>>    x=2000/50   >>>x=40.0
print(x)
```

    90
    40
    2000
    40.0
    


```python
# Relational / Comparison Operators in Python. Relational operators are used to compare two values.
# The Result of every relational operator is always a Boolean value: True or False
x=10
y=20

print(x==y) #Equal to == operator checks whether two values are equal.
print(x>y)  #Greater Than > operator checks whether the left-hand value is greater than the right-hand value.
print(x<y) #Less Than < operator checks whether the left-hand value is less than the right-hand value.
print(x>=y) #Greater Than or Equal To >= operator checks two conditions:
                                                      # Left value is greater than the right value
                                                      #OR both values are equal
print(x<=y) #less Than or Equal To <= operator checks two conditions:
                                                      # Left value is less than the rigt value
                                                      # OR both values are equal
print(x!=y) #Not Equal To != operator checks whether two values are different.
```

    False
    False
    True
    False
    True
    True
    


```python
#AND

FC          SC          Result
T           T           T
T           F           F
F           T           F


#OR
T           T           T
T           F           T
F           T           T
F           F           F
```


```python
# Logical and Operator in Python:
# The and operator is used to combine two or more conditions. and = BOTH conditions must be True.
x=10
y=20
print(x<y and y>x)
print(x<y and x==y)
print(x>y and x<y)
print(x>y and x==y)
```

    True
    False
    False
    False
    


```python
# Logical and Operator in Python:
# The or operator is used to combine two or more conditions. or = At least one condition must be True.
x=10
y=20
print(x<y or y>x)
print(x<y or x==y)
print(x>y or x<y)
print(x==y or y<x)
```

    True
    True
    True
    False
    


```python
#Membership Operators in Python
#Membership operators are used to check whether a particular value exists inside a collection or sequence.
# Python provides two main membership operators: 1). in 2). not in
data=[10,20,30,40,50]
print(10 in data) #The in operator checks whether a particular value exists inside a collection or not.
print(100 in data) # If the value is present -> True and If the value is not present -> Flase
```

    True
    False
    


```python
# not in operator
# The not in operator checks whether a value does exist inside a collection.
data=[10,20,30,40,50]
print(10 not in data) # If the value is present -> False
print(100 not in data) # If the value is not present -> True

# Imporatnt Point:
    #Membership operators can commonly be used with: List, Tuple, String, Set, Dictionary
```

    False
    True
    


```python
num1=10
num2=10
print(num1==num2)
#print(num1 is num2) #False
print(id(num1))
print(id(num2))
```

    True
    140705511285960
    140705511285960
    


```python
x=10 #Python creates an integer object containing 10.
y=20 #Now y refers to the integer object 20.

print(id(x))
print(id(y))

y=30 # The variable y is now referring to the object 30.
print(id(y)) # So the ID printed for y changes because y is now referring to a different object.

z=20 # In typical Python implementations, especially CPython, small integers such as 20 are commonly reused/cached.
    # So z can refer to the same 20 object that was previously referenced by y.
print(id(z)) #giving the same ID that y had when y was referring to 20.
```

    140705511285960
    140705511286280
    140705511286600
    140705511286280
    


```python
x=[10,20] #Python creates a list object in memory.
y=x #Python does not create another list. Instead, y refers to the same list object.
#So, both x and y point to the same object.
print(x is y) #True Why? Because x and y refers to the same list object.
#is Operator:The is  operator checks whether two variables refers to the same object in memory.
print(id(x))
print(id(y))
print(x==y) # -- Operator checks value/content equality.
```

    True
    1645454139456
    1645454139456
    True
    


```python
#== vs is with list
x=[10,20] #Python creates a list object in memory and x refers to that object.
y=[10,20] #Python creates another separate list object. Although the values are the same, the two lists are different objects.
          #Because list belngs to mutable Type.
print(x==y)     # Output:True    Why? The == Operator compares the values/content of two objects.
print(x is y)   # Output:False   Why? The is Operator checks object identity.
x.append(33)    # The list is referred to by x is modified.only the x list changes because  x and y refers to different list objects.
print(x==y)     # Output: False Because: x -> [10, 20, 33]  y -> [10,20] Their contents are now different.
print(id(x))
print(id(y))
```

    True
    False
    False
    1645454140928
    1645454315456
    


```python
x=10 # x refers to the integer object 10.
y=10 # Python can make y refer to the same integer object 10.
print(id(x))
print(id(y))
print(x==y) # Therefore: id(x) == id(y) is typically: True
print(x is y) #And: x is y returns: True because x and y refer to the same object.

# Note: For integers and same other immutable objects, Python may refuse objects, but you should generally use == to compare values
# and use is mainly when checking object identity
```

    140703468135624
    140703468135624
    True
    True
    


```python
# Membership Operators: in and out in
# Membership Operators: are used to check whether a particular value exists inside a sequence or collection, such as a list, tuple, string, set, etc.

data=[10,20,30,66,88]
print(22 in data) #checks whether a value does not exist, It returns either True or False.
print(20 in data)
```

    False
    True
    


```python
data=[10,20,30,66,88]
print(22 not in data) #checks whether a value does not exist, It returns either True or False.
print(20 not in data)
```

    True
    False
    


```python
#Important for Python: Python does not support:
i++ #Post-increment
++i #Pre-increment

i-- #Post-decrement
--i #Pre-decrement

# Python, use:
i += 1
i -= 1
```


```python
age=int(input("Enter User Age"))
print(type(age))
```

    Enter User Age 20
    

    <class 'int'>
    


```python
age=int(input("Enter User Age"))
if(age>=18):
    print("Valid for voting")
```

    Enter User Age 25
    

    Valid for voting
    


```python
#if else block
age=int(input("Enter User Age"))
if(age>=18):
    print("Valid for Voting")
else:
    print("Not Valid for Vote")
```

    Enter User Age 10
    

    Not Valid for Vote
    


```python
#To check Even or Odd Number
num=int(input("Enter Number"))
if(num%2==0):
    print("Number is Even")
else:
    print("Number is Odd")
```

    Enter Number 567
    

    Number is Odd
    


```python
#To check Number is positive or Negative
num=int(input("Enter Number"))
if(num>0):
    print("Number is Positive")
else:
    print("Number is Negative")
```

    Enter Number 10
    

    Number is Positive
    


```python
#if elif else statement
marks=int(input("Enter Marks: "))
if(marks>=90):
    print("Grade A")
elif(marks>=80):
    print("Grade B")
elif(marks>=70):
    print("Grade C")
elif(marks>=60):
    print("Grade D")
else:
    print("Fail")
```

    Enter Marks:  77
    

    Grade C
    


```python
age=int(input("Enter Age:"))
idPass=False
if(age>=18):
    if(idPass==True):
        print("Study Entry Allowed")
    else:
        print("Student have no ID. Entry Not Allowed")
else:
    print("Student age is not valid. Entry Not Allowed")
```

    Enter Age: 22
    

    Student have no ID. Entry Not Allowed
    


```python
#Exercise 1: ATM Withdrawl
#Write a Java Program for ATM withdrawal.
#Conditions:
#Check whether PIN is correct.
#If PIN IS correct:
#Check whether withdrawal amount is a multiple of 100.
#If yes, check whether balance is sufficient.
#If sufficient,withdraw the amount.
#otherwise print "Insufficient Balance"
#If PIN is incorrect, print "Invalid PIN"

balance=25000
pin=int(input("Enter Your Pin"))
if(pin==1234):
    amount=int(input("What amount do you want to withdraw"))
    if(amount%100==0):
        if(amount<=balance):
            balance-=amount # balance-balance-amount
            print("Withdraw amount is:", amount)
            print("Remaining balance is:", balance)
        else:
            print("Paisa Nahi hai")
    else:
        print("Invalid amount")
else:
    print("Incorrect Pin")
```

    Enter Your Pin 1234
    What amount do you want to withdraw 2000
    

    Withdraw amount is: 2000
    Remaining balance is: 23000
    


```python
#Exercise 2: Student Result System
#Write a program that takes marks of 3 subjects. 
#Conditions:

#If every subject has marks >= 40:
#Calculate percentage.
#If percentage >= 75 -> Distinction
#If percentage >= 60 -> First Division 
#If percentage >= 50 -> Second Division
#Otherwise -> Pass
#If any subject is below 40 -> Fail.

java=int(input("Enter Marks of Java: "))
python=int(input("Enter Marks of Python: ")) 
dbms=int(input("Enter Marks of DBMS: "))

if(java>=40):
    if (python>=40):
        if(dbms>=40):
            totalMarks=java+python+dbms
            per=totalMarks/3
            print("Total is:" , totalMarks)
            print("Student Per :", per)
            if (per>=75):
                print("A+")
            elif (per>=60):
                print("First Division")
            elif (per>=50):
                print("Second Division")
            else:
                print("Pass")
        else:
            print("Fail in DBMS")
    else:
        print("Fail in Python")
else:
    print("Fail in Java")
```

    Enter Marks of Java:  65
    Enter Marks of Python:  77
    Enter Marks of DBMS:  45
    

    Total is: 187
    Student Per : 62.333333333333336
    First Division
    


```python
#Exercise 3: Bank Loan Eligibility 
#A bank gives a loan based on:

#Age must be >= 21.
#If age is valid:
#Salary must be >= 25,000.
#If salary is valid:
#Credit score >= 750 → Loan approved
#Credit score >= 650 → Loan approved with higher interest
#Otherwise → Loan rejected.

age=int(input("Enter Your Age: "))
salary=int(input("Enter Your Salary"))
creditScore=int(input("Enter Your Credit Score: "))

if(age>=21):
    if(salary>=25000):
        if(creditScore>=750):
            print("Loan Approved");
            print("Interest Rate: 8%");
        elif(creditScore >= 650):
            print("Loan Approved");
            print("Interest Rate: 10%");
        else:
            print("Loan Rejected")
    else:
        print("Salary is too Low")
else:
    print("Age is not eligible")
```

    Enter Your Age:  23
    Enter Your Salary 25000
    Enter Your Credit Score:  750
    

    Loan Approved
    Interest Rate: 8%
    


```python
#Exercise 4: E-Commerce Discount
#An online shopping website provides discount based on:

#If cart amount >= 5000:
#If customer is a premium member:
#Discount = 20%
#Otherwise:
#Discount = 10%
#If cart amount < 5000: 
#If premium member:
#Discount = 5%
#Otherwise:
#No discount.

#Print final amount.

amount=8000
pMember=True
if(amount>=5000):
    if (pMember):
        discount=amount*20/100
        print("Discount amount is: ", discount)
    else:
        discount=amount*10/100
        print("Discount amount is: ",discount)
elif (pMember):
    discount=amount*5/100
    print("Discount amount is: ",discount)
else:
    discount=0
    print("Discount amount is: ", discount)
final_amount=amount-discount
print("Your Final Amount is: ", final_amount)
```

    Discount amount is:  1600.0
    Your Final Amount is:  6400.0
    


```python
##Exercise 5: Login + Role Based Access
#Conditions
#Username correct?
#Password correct?
#Role:
#admin → Full Access
#teacher → Teacher Dashboard
#student → Student Dashboard 
#anything else → Invalid Role

userName=input("Enter UserName: ")
password=input("Enter Password: ")
role=input("Enter Role: ")
if(userName=="Admin"):
    if(password=="12345"):
        if(role=="Admin"):
            print("You Have Full Access")
        elif (role=="Trainer"):
            print("Trainer Dashboard")
        elif(role=="Student"):
            print("Student Dashboard")
        else:
            print("Invalid Role")
    else:
        print("Invalid Password")
else:
    print("Invalid User Name")
```

    Enter UserName:  Admin
    Enter Password:  12345
    Enter Role:  Trainer
    

    Trainer Dashboard
    

Exercise 1: Electricity Bill
Conditions:
0-100        →  ₹5/unit
101-200      →  ₹7/unit
201-300      →  ₹10/unit
Above 300    →  ₹15/unit

Additionally:
Bill > ₹3000 → 10% surcharge

Exercise 2: Employee Bonus
Conditions
Experience >= 1 year
Salary >= ₹50,000:
Performance >= 90 → 20%
Performance >= 75 → 10%
otherwise → 5%
Salary < ₹50,000:
Performance >= 90 → 15%
Otherwise → 5%

Exercise 3: Driving License
Conditions
Age >= 18
Learner license available?
Driving test score >= 60

Exercise 4: ATM - Difficult Challenge
Conditions
PIN correct
Account active
Amount positive
Amount multiple of ₹100
Balance sufficient
Withdrawal ke baad minimum ₹500 balance hona chahiye
Amount > ₹20,000 → Extra verification

Exercise 1: Print all even numbers from 1 to 20. 
Exercise 2: Print all odd numbers from 1 to 20.
Exercise 3: Print multiples of 5 from 5 to 50. 
Exercise 4: Find the sum of numbers from 1 to 10.
Exercise 5: Find the sum of even numbers from 1 to 100.
Exercise 6: Find the sum of odd numbers from 1 to 100.
Exercise 7: Print the multiplication table of 7.
Exercise 8: Take a number from the user and print its multiplication table.
Exercise 9: Print numbers from 1 to 100 that are divisible by both 3 and 5. 
Exercise 10: Count even and odd numbers between 1 and 50.


```python
for i in range(1,21,1):
    if(i%2==0):
        print(i)
```

    2
    4
    6
    8
    10
    12
    14
    16
    18
    20
    


```python
for i in range(2,21,2):
    print(i)
```

    2
    4
    6
    8
    10
    12
    14
    16
    18
    20
    


```python
for i in range(1,21,1):
    if(i%2!=0):
        print(i)
```

    1
    3
    5
    7
    9
    11
    13
    15
    17
    19
    


```python
for i in range(5,51,5):
    print(i)
```

    5
    10
    15
    20
    25
    30
    35
    40
    45
    50
    


```python
sum=0
for i in range(1,11,1):
    sum+=i #sum=sum+i    sum=0+1
print(sum)
```

    55
    


```python
sum=0
for i in range(1,101,1):
    if i%2==0:
        sum+=i
print(sum)
```

    2550
    


```python
table=int(input("Enter Table"))
for i in range(1,11,1):
    print(i*table)
```

    Enter Table 5
    

    5
    10
    15
    20
    25
    30
    35
    40
    45
    50
    


```python
for i in range(1,101,1):
    if i%3==0 and i%5==0:
        print(i)
```

    15
    30
    45
    60
    75
    90
    


```python
evenCount=0
oddCount=0
for i in range(1,51,1):
    if i%2==0:
        evenCount+=1
    else:
        oddCount+=1
print(evenCount)
print(oddCount)
```

    25
    25
    


```python
data=[22,54,65,23,21,45]
largeNumber=data[0]
for i in data:
    if(i>largeNumber):
        largeNumber=i
print(largeNumber)
```

    65
    


```python
data=[22,54,65,23,21,45]
print(max(data))
```

    65
    


```python
data="Programming"
count=0
for i in data:
    if i in "aeiou":
        count+=1
print(count)
```

    3
    


```python
i=1 #Initialization
while(i<=10): #Condition
    print(i)
    i+=1 #Increment / Decrement
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    


```python
i=1
while(i<=10):
    if(i%2==0):
        print(i)
    i+=1
```

    2
    4
    6
    8
    10
    


```python
i=1
while(i<=10):
    if(i%2!=0):
        print(i)
    i+=1
```

    1
    3
    5
    7
    9
    


```python
i=1
sum=0
while(i<=10):
    sum+=i
    i+=1
print(sum)
```

    55
    


```python
#Ways to Create a String
city='Lucknow'
print(city)
city[0]='A'
```

    Lucknow
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[47], line 4
          2 city='Lucknow'
          3 print(city)
    ----> 4 city[0]='A'
    

    TypeError: 'str' object does not support item assignment



```python
city='Lucknow'
print(city[0])
print(city[1])
print(city[2])
```

    L
    u
    c
    


```python
city='Lucknow'
print(city[-1])
```

    w
    


```python
city='Lucknow'
print(city[0:4])
```

    Luck
    


```python
city='Lucknow'
print(city[-3:])
```

    now
    


```python
city='Lucknow '
print(city*6)
```

    Lucknow Lucknow Lucknow Lucknow Lucknow Lucknow 
    


```python
<
>
<=
>=
==
!=
```


```python
in
not in
```


```python
data="   Zayn Zaidi   "
print(len(data))
print(data.upper())
print(data.lower())
print(data.strip())
```

    16
       ZAYN ZAIDI   
       zayn zaidi   
    Zayn Zaidi
    


```python
data="   Zayn Zaidi   "
print(data.lstrip())
```

    Zayn Zaidi   
    


```python
data="   Zayn Zaidi   "
print(data.rstrip())
```

       Zayn Zaidi
    


```python
data="I Love Python Programming"
print(data.replace('Python','Java'))
print(data)
```

    I Love Java Programming
    I Love Python Programming
    


```python
data="I Love Python Programming"
newData=data.replace('Python','Java')
print(newData)
print(data)
```

    I Love Java Programming
    I Love Python Programming
    


```python
data="I Love Python Programming"
print(data.index('P'))
print(data.find('Z'))
```

    7
    -1
    


```python
city="Bareilly"
print(*[city]*5, sep="\n")
```

    Bareilly
    Bareilly
    Bareilly
    Bareilly
    Bareilly
    


```python
print("Hello",'Hi')
```

    Hello Hi
    


```python
data="I Love Pyhton Programming"
print(data.count('P'))
```

    2
    


```python
#startswith()
email="admin@gmail.com"
print(email.startswith('admin'))
```

    True
    


```python
#endswith()
email="admin@gmail.com"
print(email.endswith('com'))
```

    True
    


```python
#spilt()
data="I Love Python Programming"
print(data.split())
```

    ['I', 'Love', 'Python', 'Programming']
    


```python
#join()
data=['I', 'Love', 'Python', 'Programming']
result=" ".join(data)
print(result)
```

    I Love Python Programming
    


```python
#isalpha()
data="Invertis"
print(data.isalpha())
```

    True
    


```python
#isdigit()
data="12345"
print(data.isdigit())
```

    True
    


```python
#isalnum()
data="Invertis123"
print(data.isalnum())
```

    True
    


```python
#isalnum()
data="Invertis123@"
print(data.isalnum())
```

    False
    


```python
#islower()
data="Invertis"
print(data.islower())
```

    False
    


```python
#islower()
data="invertis"
print(data.islower())
```

    True
    


```python
#isupper()
data="INVERTIS"
print(data.isupper())
```

    True
    


```python
count=0
i=0
data="Python Programming"
while(i<len(data)):
    if data[i]=='P':
        count+=1
    i+=1
print(count)
```

    2
    


```python
data=[22,32,45,-2,87,-1,89,-4]
posCount=0
negCount=0
i=0
while(i<len(data)):
    if data[i]>0:
        posCount+=1
    else:
        negCount+=1
    i+=1
print(posCount)
print(negCount)
```

    5
    3
    


```python
data="Python Programming p"
count=0
i=0
while(i<len(data)):
    if data[i]=="P" or data[i]=="p":
        count+=1
    i+=1
print(count)
```

    3
    


```python
data={10,23,43,22,65,78}
print(type(data))
```

    <class 'set'>
    


```python
data={10,23,43,22,65,78,43,23,10}
print(data)
print(data[0])
print(data[0:6])
```

    {65, 22, 23, 10, 43, 78}
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[24], line 3
          1 data={10,23,43,22,65,78,43,23,10}
          2 print(data)
    ----> 3 print(data[0])
          4 print(data[0:6])
    

    TypeError: 'set' object is not subscriptable



```python
data={10,23,43,22,65,78}
print(data)
```

    {65, 22, 23, 10, 43, 78}
    


```python
#add()
data={10,23,43,22,65,78}
data.add(45)
print(data)
```

    {65, 22, 23, 10, 43, 45, 78}
    


```python
#update()
data={10,23,43,22,65,78}
data.update([10,20,30])
print(data)

data.remove(43)
print(data)

#data.remove(55) keyError          Traceback (most recent call last)
#print(data)

#discard()
data.discard(55)
print(data)

#pop()
data.pop()
```

    {65, 20, 30, 22, 23, 10, 43, 78}
    {65, 20, 30, 22, 23, 10, 78}
    {65, 20, 30, 22, 23, 10, 78}
    




    65




```python
#pop()
data={10,23,43,22,65,78}
data.pop() #65
print(data)
```

    {22, 23, 10, 43, 78}
    


```python
#clear()
data={10,23,43,22,65,78}
data.clear()
print(data)
```

    set()
    


```python
data={}
print(type(data))
```

    <class 'dict'>
    


```python
data=set()
print(type(data))
```

    <class 'set'>
    


```python
#copy()
data={10,23,43,22,65,78}
newData=data
print(newData)

copydata=data.copy()
print(copydata)
```

    {65, 22, 23, 10, 43, 78}
    {65, 22, 23, 10, 43, 78}
    


```python
#Union
A={10,20,30}
B={30,40,50}
print(A.union(B))
print(A|B)

print("--------------------")
print(A.intersection(B))
print(A&B)

print("--------------------")
print(A.difference(B))
print(A-B)
```

    {50, 20, 40, 10, 30}
    {50, 20, 40, 10, 30}
    --------------------
    {30}
    {30}
    --------------------
    {10, 20}
    {10, 20}
    


```python
len()
max()
min()
sum()
```


```python
count=0
i=0
data="Python Programming"
while(i<len(data)):
    if data[i]=='P':
        count+=1
    i+=1
print(count)
```

    2
    


```python
data="invertis@123"
remove="@"
#result="inv"
result=""
for char in data:
    if char != remove:
        result+=char
print(result)
```

    invertis123
    


```python
data="invertis@123"
#result="invertis123"
result=""
i = 0
while i < len(data):
    if data[i] != "@":
        result+=data[i]
    i += 1
print(result)
```

    invertis123
    


```python
#Duplicate Key not allowed.
data={"name":"Zayn","age":23,"college":"Invertis","name":"Zatch"}
print(data)
```

    {'name': 'Zatch', 'age': 23, 'college': 'Invertis'}
    


```python
#Mutable
data={"name":"Zayn","age":23,"college":"Invertis"}
data["name"]="Luffy"
print(data)
```

    {'name': 'Luffy', 'age': 23, 'college': 'Invertis'}
    


```python
#valid Keys
data={1:"Zatch", "Age":23, 2.3: "Version"}
print(data)
```

    {1: 'Zatch', 'Age': 23, 2.3: 'Version'}
    


```python
#invalid Keys
data={[1,2]:"Version"}
print(data)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[46], line 2
          1 #invalid Keys
    ----> 2 data={[1,2]:"Version"}
          3 print(data)
    

    TypeError: unhashable type: 'list'



```python
#empty Dict
data={}
print(type(data))

data=dict()
print(type(data))
```

    <class 'dict'>
    <class 'dict'>
    


```python
#Acccessing Values
data={"name":"Zayn","age":23,"college":"Invertis"}
#Method 1: Using Keys
print(data["name"])
#print(data["Version"])

#Method 2: Using get() method
print(data.get("name"))
print(data.get("Version"))
```

    Zayn
    Zayn
    None
    


```python
#Adding New Element
data={"name":"Zayn","age":23,"college":"Invertis"}
data["course"]="Python Programming"

print(data)
```

    {'name': 'Zayn', 'age': 23, 'college': 'Invertis', 'course': 'Python Programming'}
    


```python
#Updating Values
data={"name":"Zayn","age":23,"college":"Invertis"}
data.update({"name": "Zatch","age":25})
print(data)
```

    {'name': 'Zatch', 'age': 25, 'college': 'Invertis'}
    


```python
#len()
data={"name":"Zayn","age":23,"college":"Invertis"}
print(len(data))
```

    3
    


```python
#keys()
data={"name":"Zayn","age":23,"college":"Invertis"}
print(data.keys())
```

    dict_keys(['name', 'age', 'college'])
    


```python
#values()
data={"name":"Zayn","age":23,"college":"Invertis"}
print(data.values())
```

    dict_values(['Zayn', 23, 'Invertis'])
    


```python
#items()
data={"name":"Zayn","age":23,"college":"Invertis"}
print(data.items())
```

    dict_items([('name', 'Zayn'), ('age', 23), ('college', 'Invertis')])
    


```python
#pop()
data={"name":"Zayn","age":23,"college":"Invertis"}
data.pop("age")
print(data)
```

    {'name': 'Zayn', 'college': 'Invertis'}
    


```python
#clear()
data={"name":"Zayn","age":23,"college":"Invertis"}
data.clear()
print(data)
```

    {}
    


```python
#copy
data={"name":"Zayn","age":23,"college":"Invertis"}
newData=data.copy()

data["name"]="Zatch"
print(data)
print(newData)

```

    {'name': 'Zatch', 'age': 23, 'college': 'Invertis'}
    {'name': 'Zayn', 'age': 23, 'college': 'Invertis'}
    


```python
#Membership
data={"name":"Zayn","age":23,"college":"Invertis"}
print("age" not in data)
print("course" not in data)
```

    False
    True
    

1. Check Student Result   

Question:
Given a dictionary containing student marks, use a loop to print whether each student has Passed or Failed.   

Condition:   

Marks >= 40 → Pass
Marks < 40 → Fail
students = {
    "Rahul": 75,
    "Amit": 32,
    "Priya": 88,
    "Neha": 39,
    "Rohit": 55
}   

2. Student Performance Using Nested If   

Question:
Print the performance category of each student.   

Conditions:   

Marks >= 80 → Excellent
Marks >= 60 → Good
Marks >= 40 → Average
Marks < 40 → Fail
students = {
    "Rahul": 85,
    "Amit": 35,
    "Priya": 72,
    "Neha": 48
}   

3.Product Stock Management   

Question:
A dictionary contains products and their available stock. Use a loop and nested conditions to display the stock status.   

Conditions:   

Stock = 0 → Out of Stock
Stock <= 5 → Low Stock
Stock > 5 → Available
products = {
    "Laptop": 10,
    "Mouse": 3,
    "Keyboard": 0,
    "Monitor": 7,
    "Printer": 2
}   

4. Employee Salary and Department   

Question:
The following dictionary contains employee salary and department. Display the employee category.   

Conditions:   

Salary >= 50,000:
IT -> Senior IT Employee
HR -> Senior HR Employee
Other department -> Senior Employee
Salary < 50,000 -> Junior Employee
employees = {
    "Rahul": {"salary": 60000, "department": "IT"},
    "Amit": {"salary": 40000, "department": "HR"},
    "Priya": {"salary": 70000, "department": "IT"},
    "Neha": {"salary": 45000, "department": "Finance"}
}   

4.Check Even/Odd Values   

Question:
Given a dictionary, check whether each value is even or odd.   

If the value is:   

Even and greater than 20 → Large Even
Even and <= 20 → Even
Odd → Odd
data = {
    "a": 10,
    "b": 15,
    "c": 25,
    "d": 30,
    "e": 40
}   

6.Shopping Cart Classification   

Question:
A dictionary contains products and their prices.

Conditions:   

Price >= 1000:
Price >= 5000 → Premium Product
Otherwise → Expensive Product
Price < 1000 → Affordable Product
products = {
    "Mobile": 15000,
    "Mouse": 500,
    "Laptop": 60000,
    "Keyboard": 1200
}   

7.Student Eligibility   

Question:
The dictionary contains student attendance and marks.   

Conditions:   

Attendance >= 75:
Marks >= 40 → Eligible
Marks < 40 → Failed in Exam
Attendance < 75 → Not Eligible
students = {
    "Rahul": {"attendance": 85, "marks": 70},
    "Amit": {"attendance": 60, "marks": 80},
    "Priya": {"attendance": 90, "marks": 35},
    "Neha": {"attendance": 78, "marks": 55}
}   

8.Bank Account Classification   

Question:
A dictionary contains customer names and account balances.   

Conditions:   

Balance > 0:
Balance >= 10,000 -> Premium Account
Otherwise → Regular Account
Balance = 0 → No Balance
Balance < 0 → Overdraft
accounts = {
    "Rahul": 25000,
    "Amit": 5000,
    "Priya": 0,
    "Neha": -2000
}   

9.Nested Dictionary - Employee Experience   

Question:
Classify employees based on salary and experience.   

Conditions:   

Salary >= 50,000:
Experience >= 5 → Senior
Otherwise → Mid-level
Salary < 50,000:
Experience >= 3 → Experienced Junior
Otherwise → Fresher/Junior

Question 10:
The following dictionary contains students' marks and attendance.   

students = {
    "Rahul": {"marks": 85, "attendance": 90},
    "Amit": {"marks": 35, "attendance": 80},
    "Priya": {"marks": 65, "attendance": 70},
    "Neha": {"marks": 45, "attendance": 85},
    "Rohit": {"marks": 90, "attendance": 60}
}   

Conditions:   

If attendance < 75 → Not Eligible
If attendance >= 75:
Marks >= 80 → Distinction
Marks >= 60 → First Division
Marks >= 40 → Pass
Marks < 40 → Fail   

Expected Output:   

Rahul Distinction
Amit Fail
Priya Not Eligible
Neha Pass
Rohit Not Eligible   


```python
students = {
    "Rahul": 75,
    "Amit": 32,
    "Priya": 88,
    "Neha": 39,
    "Rohit": 55
}   

for name, Marks in students.items():
    if(Marks >= 40):
        print(name, "Pass")
    else:
        print(name, "Fail")
```

    Rahul Pass
    Amit Fail
    Priya Pass
    Neha Fail
    Rohit Pass
    


```python
students = {
    "Rahul": 85,
    "Amit": 35,
    "Priya": 72,
    "Neha": 48
}   

for name, Marks in students.items():
    if(Marks >= 40):
        if(Marks>=80):
            print(name, "Excellent")
        elif(Marks>=60):
            print(name, "Good")
        elif(Marks>=40):
            print(name, "Average")
    else:
        print(name, "Average")
```

    Rahul Excellent
    Amit Average
    Priya Good
    Neha Average
    


```python
products = {
    "Laptop": 10,
    "Mouse": 3,
    "Keyboard": 0,
    "Monitor": 7,
    "Printer": 2
}   

for productName, stock in products.items():
    if stock==0:
        print(productName, "is Out of Stock")
    elif(stock<=5):
        print(productName, "is Low Stock")
    else:
        print(productName, "is Available")
```

    Laptop is Available
    Mouse is Low Stock
    Keyboard is Out of Stock
    Monitor is Available
    Printer is Low Stock
    


```python
employees = {
    "Rahul": {"salary": 60000, "department": "IT"},
    "Amit": {"salary": 40000, "department": "HR"},
    "Priya": {"salary": 70000, "department": "IT"},
    "Neha": {"salary": 45000, "department": "Finance"}
} 

for name,data in employees.items():
    salary=data["salary"]
    department=data["department"]
    if(salary>=50000):
        if department=="IT":
            print(name," Senior IT Employee")
        elif department=="HR":
            print(name," Senior HR Employee")
        else:
            print(name," Senior Employee")
    else:
        print(name," Junior Employee")
```

    Rahul  Senior IT Employee
    Amit  Junior Employee
    Priya  Senior IT Employee
    Neha  Junior Employee
    


```python
n=4
for i in range(n):
    for j in range(n):
        print("*", end=" ")
    print(end='\n')
```

    * * * * 
    * * * * 
    * * * * 
    * * * * 
    


```python
n=int(input("Enter No of rows: "))
for i in range(n):
    for j in range(n):
        print("*", end=" ")
    print(end='\n')
```

    Enter No of rows:  4
    

    * * * * 
    * * * * 
    * * * * 
    * * * * 
    


```python
rows=int(input("Enter No of rows: "))
columns=int(input("Enter No of columns: "))
for i in range(rows):
    for j in range(columns):
        print("*", end=" ")
    print(end='\n')
```

    Enter No of rows:  4
    Enter No of columns:  6
    

    * * * * * * 
    * * * * * * 
    * * * * * * 
    * * * * * * 
    


```python
# *
# * *
# * * *
# * * * *
# * * * * *

n=5
for i in range(1, n+1):
    for j in range(i):
        print("*", end=" ")
    print(end="\n")
```

    * 
    * * 
    * * * 
    * * * * 
    * * * * * 
    


```python
# * * * * *
# * * * *
# * * *
# * *
# *

n=5
for i in range(n, 0,-1):
    for j in range(i):
        print("*", end=" ")
    print(end="\n")
```

    * * * * * 
    * * * * 
    * * * 
    * * 
    * 
    


```python

```
