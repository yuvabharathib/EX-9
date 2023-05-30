# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER
DATE :03-05-2023

# AIM :
To write a python program for creating Chat using TCP Sockets Links.

# ALGORITHM :
```
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the Socket module in server
4.Send and receive the message using the send function in socket.
```
# PROGRAM :
## CLIENT :
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
   ```
## SERVER :
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
# OUTPUT :
## CLIENT :
![image](https://github.com/yuvabharathib/EX-9/assets/113497404/3f31eefb-a793-45e0-84ec-5558253915cf)


## SERVER :
![image](https://github.com/yuvabharathib/EX-9/assets/113497404/be0e1596-c762-40e5-b732-f600854f9f6a)


# RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.

