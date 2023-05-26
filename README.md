# APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

# EXP: 9

# DATE:03-05-2023

# AIM:
To write a python program for creating Chat using TCP Sockets Links.

# ALGORITHM:
# Client:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
server
4. Send and receive the message using the send function in socket.
# PROGRAM:
# CLIENT:
```python3
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
  ```
# SERVER:
```python3
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
   
# CLIENT OUTPUT : 
![26c06639-5e3a-45e6-b438-69b16cf62818](https://github.com/karthick960/EX-9/assets/121215938/aee6347f-aff7-44f5-85e0-bdfc9f803220)


# SERVER OUTPUT :
![a71efdc2-813a-4817-8f1e-367d554b3060](https://github.com/karthick960/EX-9/assets/121215938/ee41cc64-b32a-4f62-8b29-1a7e49bd1c3f)



# RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully
created and executed.
