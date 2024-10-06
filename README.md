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
### Client.py
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
~~~
### Server.py
~~~
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
~~~
## OUPUT
### Client
![client-output](https://github.com/user-attachments/assets/fe77a0fd-12df-4cdb-be58-bcfb09a4c306)

### Server
![Server-output](https://github.com/user-attachments/assets/379a334e-b309-4532-9c2a-4e030295245f)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
