# importing module
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



importing module
import socket
import threading

HOST="127.0.0.1"
PORT=6000

# listen for message from user
def scan_from_server(c):
    while True:
        response=c.recv(500).decode('utf-8')
        if response!='':
            user = response.split(" # ")[0]
            tokan =response.split(" # ")[1]

            print(f"[{user}]    {tokan}")
        else:
            print("Message is empty")


def voice_of_server(c):
    while True:
        response = input("# ")
        if(response!=''):
            c.sendall(response.encode())
        else:
            print("Empty message!!!")
            exit(0)

def listen_server(c):
    user = input("Enter username = ")
    if(user!=''):
        c.sendall(user.encode())
    else:
        print("Username is empty")
        exit(0)

    threading.Thread(target=scan_from_server,args=(c, )).start()
    voice_of_server(c)


def main():
    c=socket.socket(socket.AF_INET,socket.SOCK_STREAM)
    try:
        c.connect((HOST,PORT))              # V-1
        print("connected to server")
    except:
        print("Unable to connect")

    listen_server(c)

if(__name__=="__main__"):
    main()

# threading is used to send message            ****
