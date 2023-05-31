# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

# DATE:15-03-2023

# AIM :
To write a python program to perform stop and wait protocol


# ALGORITHM :
1.Start the program.
2.Get the frame size from the user
3.To create the frame based on the user request.
4.To send frames to server from the client side.
5.If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client.
6.Stop the program


# PROGRAM :
# CLIENT :
```
# Developed by : S.Bhuvaneshwari
# Register Number : 212221240010
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
 print(ack)
 continue
 else:
 c.close()
 break
 ```
# SERVER :
```
# Developed by : S.BHUVANESHWARI
# Register Number : 212221240010
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Received".encode())
 ```

# OUTPUT :
# CLIENT :
![241978639-8e7df6ed-7abd-446b-9667-bd24b898d55d](https://github.com/Bhuvaneshwari-2003/EX-2/assets/94828604/5e3db979-dc45-41d4-b6f6-1bc44005acaf)

# SERVER :
![241978343-f5f37f9f-58cd-444c-9617-739e4244871f](https://github.com/Bhuvaneshwari-2003/EX-2/assets/94828604/4470e7c7-1ce6-4fe3-a925-523f5ad6db6c)





# RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.



