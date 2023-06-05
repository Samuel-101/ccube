```
#!/bin/bash

f="users.txt"
                                            #initializing the variables for each kingdoms
k=0
m=0
u=0
h=0

while read -r line                         #while loop to read the lines in the users.txt
do
    if [[ $line == *553* ]]; then          #if condition to check if number is there in the line.
        ((k=k+1))                          #increments the value of the variable with 1 wh nif condition is true
    fi

    if [[ $line == *828* ]]; then
        ((m=m+1))
    fi

    if [[ $line == *723* ]]; then
        ((u=u+1))
    fi

    if [[ $line == *698* ]]; then
        ((h=h+1))
    fi
done < "$f"                              #used to input users.txt in the while loop.


t=$((k+m+u+h))                          #we add the numbers and store it in a variable t.

echo "Total count of user IDs are: $t"  # output 

 
```

line-4:stores the data in users.txt  into a variable 'f'.


line6-9:initialize 4 variables k,m,u,h representing the 4 kingdoms .


line11:using while loop to read each line of the users.txt which is stored in f.


line13,17,21,25:using if conditional operator and checking if any lines have the required ID.
 
 
 line14,18,22,26:incrementing the value of the variable when if condition is true  
 
 
line29: initialise the vairable f into the loop hich contains users.txt
 
 
line31: sums up all the value of the variables and stores it into t.
 
 
line33: printing t

