# Scanner-port
import socket

s = socket.socket(socket.AF_INET,socket.SOCK_STREAM)
s.settimeout(10)

host = input( "Entrer l'adresse IP a scan :")
port = int(input("Entrer le numéro du port a scan: "))

def PortScanner(port):
    if s.connect_ex((host,port)):
        print(" Le port est fermé")
    else :
        print("Le port est ouvert")

PortScanner(port)

