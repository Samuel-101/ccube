
def binary(t):<br>
    bin_text=""<br>
    for k in t:<br>
        bin_text += bin(ord(k))[2:].zfill(8)<br>
    return bin_text<br>

def hi(c,v):<br>
    u=binary(c)<br>
    v=binary(k)<br>
    r= 1 + (len(u) // len(v))<br>
    v= v* r<br>
    v = v[:len(u)]<br>
    a=''<br>
    for i in range(len(v)):<br>
         if (u[i] == v[i]):<br>
            a+= "0"<br>
         else:<br>
            a+= "1" <br>
    a=bytes(a,'utf-8')<br>
    l=[]<br>
    for i in range(0,len(a), 8):<br>
       l.append(a[i:i+8])<br>
    hug=""<br>
    for i in l:<br>
     hug += chr(int(i,2))<br>
    return hug<br>
c ="|OP `Z<E] |Y\ $"<br>
k ="Jai Shree Ram!"<br>
print(hi(c,k))<br>
'''
made a functipn to convert string into binary


defined a fucntion hi


made both of the arguments taken into binary


line-11to13:used repetition of the key and cut the extra length of the key


line 15 to 19:made them into binary string

then made them into bytes

line21 to 23:took 8 of the bytes and appended into a list.

then it converts the list into a string and returns it.
'''

