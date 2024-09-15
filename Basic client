#importing module
import socket
import threading

HOST="127.0.0.1"
PORT=6000
def main():
    c=socket.socket(socket.AF_INET,socket.SOCK_STREAM)
    try:
        c.connect((HOST,PORT))
        print("connected to server")
    except:
        print("Unable to connect")
if(__name__=="__main__"):
    main()
