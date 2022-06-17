# RSPE ( Remote Shell and Python Execution )

## About RSPE 

RSPE is an ethical hacking tool that uses python's socket library to connect to remote pcs which have the client installed on them.

This tool allows you to execute remote shell commands and python scripts on the connected pc.

This program is not specific to python and might change to other languages as well, like c++, for example.

## Dev(s) at RSPE

General: Drags

## How Does it WORK? 

### The IDEA behind RSPE

This program is NOT a reverse shell.

while at night, i got an idea, if the client can connect to the server at any point of time in reverse shell, and the server HAS firewall, it can still access it right? (thats reverse shell)

so that is limited only when the server is active.

what if whenever the client (remote) computer is up and online, the client hosts the server and the (attacker) can connect to it anytime he/she/it wants

### serious programmer stuff

when the client program is run for the first time, it copies itself into the user/username directory to make sure that the program is working even if the main downloaded stuff is deleted

after doing so, it will register itself to launch itself automatically when the system starts

whenever internet is available, it starts a server using socket and listens for incoming connections from any ip. 

for security purposes, it asks the password.

then the password is sent to client from the incoming pc to verify it

if verified, the client shows up an input in which you can enter what you want to do (* read more)

to execute shell commands, type 'sh' and your command
example:
    'sh dir'

to execute python script, just type your command
example:
    'print("i am remotely executing this")'

to execute a python script FILE, type 'loads' and then the file name
example:
    'loads path/to/yourscript.py'
note:
    for better usage do not include spaces whenever possible


then the client executes the command as per the specifications and if possible, returns the result

## DISADVANTAGES

1. You cannot use interactive stuff that require the client ask for input, this will cause delay to execute next command
example:
    'sh date'
    it causes to prompt the client to input the user which makes the sender pc to wait till the user enters something onto the client, so better use python         scripting
