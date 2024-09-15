#importing modules

import socket
import threading

HOST="127.0.0.1"
PORT=6000

def main():
    #sockets(IPV4 , TCP)
    s=socket.socket(socket.AF_INET,socket.SOCK_STREAM)

    try:
        s.bind((HOST,PORT))

    except:
        print(f"Error ! HOST = {HOST} PORT ={PORT}")
    
    s.listen(5)

    while True:
        c,address=s.accept()   # address = tuple (HOST  , PORT) of client
        print("CONNECTED to client")

    
if(__name__=="__main__"):
    main()
