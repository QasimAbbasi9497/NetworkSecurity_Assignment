
# ifconfig

> on windows open cmd as administrator and type **ipconfig**

**OR**

> on linux open your favorite terminal emulator and type **ifconfig**

![Alt text](assets/Pasted%20image%2020230108184344.png)


# Ping

> To capture arp package please install wireshark on your machine 

> For Windows installations :

1. open windows powershell as administrator and past this command
```powershell
winget install WiresharkFoundation.Wireshark
```

**Note :**You can also download wireshark from its website just open google and search wireshark download.  

![Alt text](assets/Pasted%20image%2020230108191037.png)

in this pic you can see there is no any kind of network interface is availabe.

If you want to solve this problem than follow given this note.

**note :** after installation on wireshark please check **Npcap** is installed or not. If **Npcap** is not installed with Wireshark than install it manaually from its website becaure it is very import for wireshark without **Npcap** wireshark can`t capture packet.

if you still face this problem than Right click on wireshark icon and Run wireshark as **Run as Administration** .
2. You can also Download wireshark from its offical website and install it manually.

> For Linux installation :

1. open terminal 
```bash
sudo apt install wireshark
```

for arch based 

```bash
sudo pacman -Sy wireshark
```

![Alt text](assets/Pasted%20image%2020230108191319.png)

for Linux user follow this step to view all network interface 
1. open terminal and open wireshark by using sudo command
```bash
sudo wireshark
```



> Select network interface card 

![Alt text](assets/Pasted%20image%2020230108192956.png)

## Ping Start from hare
**Note : **  Before Ping command please start wireshark select network interface card and start packet capturing

> Open terminal or cmd and type this command 

```bash
ping -c5 8.8.8.8
```

![Alt text](assets/Pasted%20image%2020230108193824.png)

> open wireshark and see this ping packet 

```
ip.src == 192.168.100. && ip.dst == 9.9.9.9
```
```
ip.src == "Your Ip Address" && ip.dst == "Ip which you ping from your terminal"
```

![Alt text](assets/Pasted%20image%2020230108194040.png)

# Arp
1. open terminal or cmd and tpye this command 

```bash
arp 192.168.100.1
```

But change ip address  before running this command 

```
arp "your default gatway Address"
```

![Alt text](assets/Pasted%20image%2020230108195105.png)

2. packet in wireshark

![Alt text](assets/Pasted%20image%2020230108195732.png)

# nslookup

> in terminal type 

```bash
nslookup google.com
```

![Alt text](assets/Pasted%20image%2020230108204213.png)

> in wireshark

```
dns contains "google"
```

![Alt text](assets/Pasted%20image%2020230108204409.png)

# traceroute on Linux
# tracert on Windows


> in terminal type 

```bash
traceroute 8.8.8.8
```

![Alt text](assets/Pasted%20image%2020230108205113.png)

> wireshark

![Alt text](assets/Pasted%20image%2020230108210301.png)

# Route

> in terminal type 
```bash
route
```

![Alt text](assets/Pasted%20image%2020230108210537.png)