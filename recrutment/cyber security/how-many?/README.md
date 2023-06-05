```
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
```

line-4:stores the data in users.txt  into a variable 'f'.


line6-9:initialize 4 variables k,m,u,h representing the 4 kingdoms .


line11:using while loop to read each line of the users.txt which is stored in f.


line13,17,21,25:using if conditional operator and checking if any lines have the required ID.
 
 
 line14,18,22,26:incrementing the value of the variable when if condition is true  
 
 
line29: initialise the vairable f into the loop hich contains users.txt
 
 
line31: sums up all the value of the variables and stores it into t.
 
 
line33: printing t

