# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
Client.py:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
Sever.py:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```
## OUPUT:
Client.py:

<img width="849" height="170" alt="image" src="https://github.com/user-attachments/assets/63806c5a-6fe6-41a5-8d9a-6f5210ba019d" />

Server.py:

<img width="835" height="169" alt="image" src="https://github.com/user-attachments/assets/b5137874-4572-489e-ae43-26ac25637ca1" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
