# Server-Cilent
## Server
    from socket import *
    serverPort = 12002
    serverSocket = socket(AF_INET6, SOCK_DGRAM)
    serverSocket.bind(('', serverPort))
    print ("-----------Exponent-----------")

    def exponent (n , m):
        return n**m

    while True:
        message, clientAddress = serverSocket.recvfrom(2048)
        n = message.decode()
        message, clientAddress = serverSocket.recvfrom(2048)
        m = message.decode()
        print('Answer : ',exponent(int(n),int(m)))
        t = str(exponent(int(n),int(m)))
        serverSocket.sendto(t.encode(), clientAddress)
## Cilent
    from socket import *
    serverName = '::1'
    serverPort = 12002
    clientSocket = socket(AF_INET6,SOCK_DGRAM)

    while True:
        message = input("Number : ")
        clientSocket.sendto(message.encode(),(serverName, serverPort))
        message = input("Exponent : ")
        clientSocket.sendto(message.encode(),(serverName, serverPort))
        msge, serverAddress = clientSocket.recvfrom(2048)
        print('Answer : ',msge.decode())
## จบ....
