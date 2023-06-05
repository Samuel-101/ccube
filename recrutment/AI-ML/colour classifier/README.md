```
def color(l):                                                         #defining a function and takesone arguement
    k=0
    u=0
    m=0
    red=[255,0,0]                                                    #initiazalizing the colour code for the 3 colours.
    blue=[0,0,255]
    green=[0,255,0]
    for i in range(len(l)):                                           #made a loop to check if the colour code is same as the inputeed one
        if(red[i]==l[i]):
            k=k+1                                                     #incremetning the value of k to find if all of them is correct
    if(k==3):                                                          #checking if the colour is same and printing it
        print("colour is red")

    for j in range(len(l)):
        if(blue[j]==l[j]):
            u=u+1
    if(u==3):
        print("colour is blue")
    for f in range(len(l)):
        if(green[f]==l[f]):
            m=m+1
    if(m==3):
        print("colour is green")
    if(k!=3 and u!=3 and m!=3):                                       #if 3 of them are not equal to 3,which means its another colour than those.
        print("it is some complex colour")
n=[0,0,255]
x =list(map(int,input("enter the numbers:").split()))                  #taking input into a list
color(x)

```

