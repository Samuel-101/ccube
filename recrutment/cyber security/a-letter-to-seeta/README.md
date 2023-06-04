Z=[]<br>
k=[]<br>
mes=input("enter:")<br>
#message = 'Nkhzn},cwe0P$wxmpp$viqiqfiv$xli$he}${lir$}sy$wipjpiwwp}$jspps{ih$qi$mrxs$xli$jsviwx0$piezmrk$filmrh$xli$gsqjsvxw$sj$xli$tepegi2Dlir$jexi$xiwxih$syv$pszi$erh$witevexih$yw0$q}$lievx$wlexxivih$mrxs$e$xlsywerh$tmigiw2$]li$temr$sj$fimrk$e{e}$jvsq$}sy0$q}$pmji+w$gsqtermsr0${ew$yrfievefpi2Pr$iziv}$qsqirx$sj$wspmxyhi0$q}$xlsyklxw$lezi$fiir$gsrwyqih$f}$}syv${ipp1fimrk2$P$tvsqmwi$}sy0$q}$fipszih0$xlex$P${mpp$rsx$viwx$yrxmp$P$lezi$jypjmppih$q}$hyx}$erh$viwxsvih$}sy$xs$}syv$vmklxjyp$tpegi$f}$q}$wmhi2\rxmp$xli$he}${i$evi$viyrmxih0$qe}$xli$kshw${exgl$sziv$}sy0$erh$qe}$}sy$jmrh$wspegi$mr$xli$ors{pihki$xlex$q}$pszi$jsv$}sy$ors{w$rs$fsyrhw2$Qsph$sr$xs$xli$qiqsvmiw$sj$syv$pszi0$jsv$xli}${mpp$wywxemr$yw$xlvsykl$xli$xvmepw$xlex$pmi$elieh2Dmxl$epp$xli$pszi$mr$q}$lievx0Fsyv$[eq' <br>
def F(input):<br>
    st=[]<br>
    for i in range (len(input)):<br>
        st.append(chr(ord(input[i])^1))<br>
    return(''.join(st))<br>
def Fu(input):    <br>
    for i in range(len(input)):<br>
        if(i<11):<br>
            Z.append(chr(ord(input[i])-i-5))<br>
        else:<br>
            Z.append(chr(ord(input[i])-4))<br>
    return(''.join(Z))<br>
def fuN(text,s):<br>
    result = ""<br>
    for i in range(len(text)):<br>
        char = text[i]<br>
        if(char.isnumeric()):<br>
            result+=(chr(ord(char)+1))<br>
        elif(char.isupper()):<br>
            result += chr((ord(char) -s-65) % 26 + 65)<br>
        else:<br>
            result+=(chr(ord(char)^1))<br>
    return result<br>
k=fuN(F(Fu(mes)), 4)<br>
print(k)<br>

'''
first we make the same 3 functions for decryption of the message.

first function we the input and makes it into ascii and then does the xor function and then makes it into the character and append it into st which is a list.

in second function,if i<11, we make the input into ascii and then subtracts it with i and 5 and then makes it into character and then appends into the list z.

for third function which has 2 arguments, we use if condition to find out if the character is numeric or an upper character or something else. If its numeric we take the ascii value and add 1 to it and then fnds the character of it. If its a upper character we take the ascii value aand substracts the key and 65 from it and if its isnt both of them,it goes into the else condition which does an XOR operation again on it.  
'''

