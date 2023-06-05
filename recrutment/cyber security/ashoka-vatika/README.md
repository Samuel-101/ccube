```
def binary(t):                                              #made a function named binary for converting them to binary
    bin_text=""
    for k in t:
        bin_text += bin(ord(k))[2:].zfill(8)        
    return bin_text

def hi(c,v):                                                   #defined a function named hi and took 2 arguments,one for key and other for the cipher text
    u=binary(c)                                                #made them to binary
    v=binary(k)
    r= 1 + (len(u) // len(v))                                  #the below three lines makes the length of the key and ciphertext which is in binary same using repetition
    v= v* r
    v = v[:len(u)]
    a=''
    for i in range(len(v)):                                    #the below code does XOR and makes them into binary string.
         if (u[i] == v[i]):
            a+= "0"
         else:
            a+= "1" 
    a=bytes(a,'utf-8')
    l=[]
    for i in range(0,len(a), 8):                                #takes 8 of the binary string and appends it into a list l
       l.append(a[i:i+8])
    hug=""
    for i in l:                                                 #makes the each element in the list into string and then returns the value
     hug += chr(int(i,2))
    return hug
c ="|OP`Z<E]|Y\$"
k ="Jai Shree Ram!"
print(hi(c,k))
```
made a functipn to convert string into binary


defined a fucntion hi


made both of the arguments taken into binary


line-11to13:used repetition of the key and cut the extra length of the key


line 15 to 19:does XOR and makes them binar string

then made them into bytes

line21 to 23:took 8 of the bytes and appended into a list.

then it converts the list into a string and returns it.
the coordinates are given in a txt file.

