```
def pattern(u):                                                 #initializing the function pattern
    p=[]                                                        
    c = 0

    for i in range(1, len(u) // 2 + 1):                         #using for loop to count and to store the value of the repeated value into a list p 
        if u[:i] == u[i:2*i]:                                    #checks if each substring is equal to its reverse
            p = u[:i]                                             #stores the string into p
            c = len(u) // len(p)                                  #counts the number of times 
            break

    if p:
        print("Pattern Found:", p)                                #prints the value of pattern and counts it.
        print("Number of times the pattern repeats :", c)             
    else:
        print("Pattern Not Found")


x =list(map(int,input("enter the numbers:").split()))           #taking input into the list 
pattern(x)                                                       #calling the function


```

