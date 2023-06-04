
#!/bin/bash                                   

f="users.txt"                                         #stores the data in users.txt  into a variable 'f'
    
k=0                                                   #initialize 4 variables k,m,u,h representing the 4 kingdoms
m=
u=0
h=0

while read -r line                                     #using while loop to read each line of the users.txt which is stored in f
do
  if [[ $line == *553* ]]; then                         #using if conditional operator and checking if any lines have the required ID
        ((k=k+1))                                       #incrementing the value of the variable when if condition is true  
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

done < "$f"                                             #initialise the vairable f into the loop hich contains users.txt

t=$((k+m+u+h))                                          #sums up all the value of the variables and stores it into t.

echo "Total count of user IDs are: $t"                   #printing t
