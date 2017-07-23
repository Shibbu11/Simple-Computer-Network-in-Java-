# Simple-Computer-Network-in-Java

This is project for Computer Networks Course implemented in Java

Classes: 
1. **Router** ( DHCP enabled):
This project has most important Class as Router which has name(Router1),interfaces and each interface has IP,Subnet Mask and Type.
Here ,type is used to distinguish between devices connected to the router which can be either of Switch,DNS or HTTP Server.
Through this project,we have tried to implement a simple network which has 2 Switches connected to Router,1 DNS and 1 HTTP Server and both of the switches have 5 Hosts connected to them.
For DHCP ,we have made a function in Router class which on being called  by Host assigns an IP address to that host. 


2.**Switch**:
This class has variables name,Rip,Rinterface,portNo.Name assigns name to switches,Rip and Rinterface denotes ip address and interface of router thorugh which this switch is connected to router.
Switch has 5 Host connected to it which are given MAC addresses ,switch identifies these hosts b thier MAC's until they are assigned IP addresses dynamically by Router.


3.**Host**:
This class has variables name,mac,ip,dg,port.
name:Name of the host
mac:MAC address of host
ip:IP address of host
dg:Default gateway for host
port:port no of switch through which it is connected to switch

**ping()** Method: This is the most important method of this class .By this,we can ping any other devices connected in the Network.
This method first sends packet to switch,switch then checks for destination in it's network ,if destination is not in switches networks then it forwards packet to Router which checks for Mode of message and according forwards it to the destination.
Mode:We have differentiated messages into 3 categories--0 for ping ,1 for HTTP request ,2 for DNS request


4.**HTTP**:
This class has a variable ip which denotes ip of the HTTP Server and a method httpRequest() which on being called by a host displyes simple message on screen.

5.**DNS**:
We have named our DNS server as www.google.com and which has ip of HTTP server and has it's own ip too.
On being called by host it calls HTTP server.Thus displays simple message on screen.

6.**NetworksProject**:
This class has **main()** method,So ,this class is driver class of this project.This class is used to actually creating the instances of other classes and for doing all the things of this projects.


***All the other methods in classes are self-explanatory.You will unterstand thier functions,once you go through them.***


I am also including an image of network (Made in Cisco Packet Tracer).


