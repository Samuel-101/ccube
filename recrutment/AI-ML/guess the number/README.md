```
import random
x=input("enter your name :")                                  #taking input for name,upper limit and lower limit
y=int(input("enter the upper limit :") )  
z=int(input("enter the lower limit :"))
a=random.randint(y,z)                                          #taking a random number from the upper limit and lower limit
print(a)
o=100                                                          #initializing the 100 points into the variaable
while True:                                                    #using while loop to run till the user looses his full points of guess the correct number
    u=int(input("enter you guess :"))                           #inputiing the guess number
    if (o==0):                                                  #using if condition to check if o becomes 0 so that he looses game and breaks the loop.
        print("sorry,you run out of points")
        break
    if(u==a):                                                    #if the user inputs the same value as the random number it prints you guess is correct and breaks the loop 
        print("your guess is correct")
        print("points u are left with :",o)
        break
    elif(u>a):                                                     #if the  guess is higher than the random number it prints to high
        print("to high")
        o=o-5
    else:
        print("to low")                                             #if the guess is to lesser than the random nuber it prints too low
        o=o-5

```
