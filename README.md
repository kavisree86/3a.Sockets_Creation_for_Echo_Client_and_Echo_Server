# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
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
## Client program
import socket    
s=socket.socket()    
s.connect(('localhost',8000))   
while True:    
 msg=input("Client > ")    
 s.send(msg.encode())   
 print("Server > ",s.recv(1024).decode())    

## Server program
import socket   
s=socket.socket()   
s.bind(('localhost',8000))   
s.listen(5)    
c,addr=s.accept()   
while True:    
 ClientMessage=c.recv(1024).decode()   
 c.send(ClientMessage.encode())    
## OUPUT
## client 
![image](https://github.com/kavisree86/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145759687/7eaceae3-b736-426a-87f2-920955bf5a5a)
## server
![image](https://github.com/kavisree86/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145759687/2ed88287-ecdd-4cd3-a236-cc3d5a02c70f)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
