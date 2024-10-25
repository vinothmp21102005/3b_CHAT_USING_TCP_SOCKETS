# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
### NAME : KARUNIYA M
### REG NO : 212223240068
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
CLIENT:
```
import socket 
s=socket.socket() 
s.connect(('localhost',90)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',90))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage) 
    msg=input("Server > ") 
    c.send(msg.encode())
```
## OUPUT
![image](https://github.com/user-attachments/assets/945d3de6-3703-4ece-9287-71eefbb50a63)

![image](https://github.com/user-attachments/assets/b10c585b-d486-4701-8c1c-254400a6b98d)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
