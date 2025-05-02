# 3b.CREATION FOR CHAT USING TCP SOCKETS
NAME : SIVA SHALINI.S
REG NO : 212224240154

## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
```
client.py
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
```
server.py
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
![WhatsApp Image 2025-05-02 at 22 51 31_e75627ab](https://github.com/user-attachments/assets/5fd54cad-764e-4360-8a82-816f4c556e77)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
