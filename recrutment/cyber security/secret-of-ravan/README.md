```
import pyzipper<br>

characters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z', '0', '1', '2', '3', '4', '5', '6', '7', '8', '9', '!', '@', '#', '$', '%', '^', '&', '*', '(', ')', '_', '-', '+', '=', '{', '}', '[', ']', '|', ';', ':', '"', "'", '<', '>', '?', ',', '.', '/', '`', '~'] 

known_password_dict = {'n': 1, '_': 2, '^': 3, '`': 5, 'W': 6, '5': 8}<br>

x = '/home/samuel/Desktop/ccube rerutment task/task_3_secret_of_ravan/The_secret.zip'<br>
l = list(known_password_dict.keys())<br>
l.insert(3, '')<br>
l.insert(6, '')<br>

for i in characters:<br>
    l[3] = i<br>
    for j in characters:<br>
        l[6] = j<br>
        d = ''.join(l)<br>
        print(d)<br>
        try:<br>
            with pyzipper.AESZipFile(x) as zf:<br>
                zf.extractall(pwd=d.encode())<br>
                print('success', d)<br>
                break<br>
        except Exception as e:<br>
            print(f"failed: {e}")<br>
```

we store the zip file in a variable 'x'

using insert function we insert spaces into the known_password_dictionary

then we use a loop to brute force and find the pasword by trying out all of the combinations possible,first we input the first chharacter and runs the second loop whick checks all the characters and so on

using try and except we use pyzipper and extracts and finds the password which hass the hint.txt.


