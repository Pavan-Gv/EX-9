# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER
```
DATE : 04-05-2023
```
### AIM :
To write a python program for creating Chat using TCP Sockets Links.

### ALGORITHM :
```
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the Socket module in server
4.Send and receive the message using the send function in socket.
```
### PROGRAM :
```
Developed By: G Venkata Pavan Kumar
Reg. No: 212221240013
```
#### Clent_Side:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
#### Server_side:
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
### OUTPUT :
#### Clent_Side:
![image](https://github.com/Pavan-Gv/EX-9/assets/94827772/c7e54cb6-b938-42ce-b78a-a139979125e6)
#### Server_side:
![image](https://github.com/Pavan-Gv/EX-9/assets/94827772/cd9cf58c-7e0a-4419-b7ef-4cba7515c806)
### RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
