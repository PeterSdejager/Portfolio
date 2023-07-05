# ELF Brute-forcing

This script was something I wrote for the National Cyber League. It was meant to brute-force the values from **SKY-AAAA-0000** all the way until **SKY-ZZZZ-9999**. The goal was for it to eventually hit the flag and give the output from the binary that the string was correct. The code did work, but it would take too long to brute-force. However, I still do believe that this code will come in handy later on for another CTF, so this is why I have it saved here.

```python
#!/usr/bin/env python3
from pwn import *
from itertools import product

uppercase=list("ABCDEFGHIJKLMNOPQRSTUVWXYZ")
numbers=list("1234567890")

binary_file = './rock' #the binary I will be brute-forcing
context(arch='amd64') # the architecture you are running the binary on

charlist = uppercase #use uppercase as the list for the characters
for c in product(charlist, repeat=4): #iterates from AAAA to ZZZZ
    x=999 				#for going from 999-9999
    while (x != 9999):
        elf = ELF(binary_file) #runs the binary every loop 
        p = process(binary_file) #makes the process every loop
        print(p.recvuntil(b'\n')) # gets the output until a new line
        string = "SKY-" + ''.join(c) + "-{}".format(x) # formats the string in a SKY-ABCD-1234 format 
        print("Testing out " + string) #output for user to see what is being tested
        p.sendline(string) #sends the string to the binary
        print(p.recvall()) # gets all of the output from the binary to check if the string is correct
        x = x+1 #goes to next number
```
