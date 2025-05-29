# 3a.ECHO CLIENT AND SERVER USING TCP SOCKETS
### Name:BALAJI J
### Reg.no:212224040042
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### client.py
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### server.py
```python
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUPUT
### client.py
![Screenshot 2025-05-09 205705](https://github.com/user-attachments/assets/94f04655-0d31-4564-bc4a-05fbd7d550b5)

### server.py
![Screenshot 2025-05-09 205714](https://github.com/user-attachments/assets/069f5aff-2a01-437b-bb3e-0a5c024bef3e)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
