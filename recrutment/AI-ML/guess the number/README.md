```
import random
x=input("enter your name :")                                  #taking input for name,upper limit and lower limit
y=int(input("enter the upper limit :") )  
z=int(input("enter the lower limit :"))
a=random.randint(y,z)                                          #
print(a)
o=100
while True:
    u=int(input("enter you guess :"))
    if (o==0):
        print("sorry,you run out of points")
        break
    if(u==a):
        print("your guess is correct")
        print("points u are left with :",o)
        break
    elif(u>a):
        print("to high")
        o=o-5
    else:
        print("to low")
        o=o-5

```
