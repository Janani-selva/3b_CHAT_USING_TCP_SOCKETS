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
## Client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## Server
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
## OUPUT
## Client
![Screenshot 2025-05-14 194458](https://github.com/user-attachments/assets/51e1ba3f-7057-4971-8db1-0c5bbf9cc848)

## Server
![Screenshot 2025-05-14 194513](https://github.com/user-attachments/assets/abd4b14f-fc5b-42ba-b48a-c9d4c52eab49)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
