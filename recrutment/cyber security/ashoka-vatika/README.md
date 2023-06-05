```
def binary(t):
    bin_text=""
    for k in t:
        bin_text += bin(ord(k))[2:].zfill(8)
    return bin_text

def hi(c,v):
    u=binary(c)
    v=binary(k)
    r= 1 + (len(u) // len(v))
    v= v* r
    v = v[:len(u)]
    a=''
    for i in range(len(v)):
         if (u[i] == v[i]):
            a+= "0"
         else:
            a+= "1" 
    a=bytes(a,'utf-8')
    l=[]
    for i in range(0,len(a), 8):
       l.append(a[i:i+8])
    hug=""
    for i in l:
     hug += chr(int(i,2))
    return hug
c ="|OP `Z<E] |Y\ $"
k ="Jai Shree Ram!"
print(hi(c,k))
```
made a functipn to convert string into binary


defined a fucntion hi


made both of the arguments taken into binary


line-11to13:used repetition of the key and cut the extra length of the key


line 15 to 19:made them into binary string

then made them into bytes

line21 to 23:took 8 of the bytes and appended into a list.

then it converts the list into a string and returns it.


