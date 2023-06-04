
#!/bin/bash                                   

f="users.txt"                                        
    
k=0                                                  
m=
u=0
h=0

while read -r line                                     
do
  if [[ $line == *553* ]]; then                         
        ((k=k+1))                                         
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

done < "$f"                                             

t=$((k+m+u+h))                                          

echo "Total count of user IDs are: $t"                   


stores the data in users.txt  into a variable 'f' \n
initialize 4 variables k,m,u,h representing the 4 kingdoms 
using while loop to read each line of the users.txt which is stored in f
 using if conditional operator and checking if any lines have the required ID
 incrementing the value of the variable when if condition is true  
 initialise the vairable f into the loop hich contains users.txt
 sums up all the value of the variables and stores it into t.
 printing t

