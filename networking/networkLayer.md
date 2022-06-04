---
layout: default
title: OSI Model
nav_order: 2
parent: Networking
---

# Unit 5 Network Layer 

Switches - link layer devices
Routes - network layer devices 
Forwarding Table

## Forwarding table 
- Router has forwarding table
- A router forwards packet by examining the value in header field  of arriving packet 
- Use this header value to index into the router’s forwarding table. 
- In table, value for that header indicates the router’s outgoing link interface to
which that packet is to be forwarded. 
- Depending network-layer protocol,the header value could be the destination address or an indication of connection to which the packet belongs.

<img src="./img/networkLayer/routing.png" width="300px" />





## Virtual-circuit and datagram

| **Virtual-circuit (VC)networks**                                                                                                                  	| **Datagram Networks**                                                                                                                         	|
|---------------------------------------------------------------------------------------------------------------------------------------------------	|-----------------------------------------------------------------------------------------------------------------------------------------------	|
| Host to host i.e handshaking                                                                                                                      	| Connection service                                                                                                                            	|
| VC setup: Each time a new connection is establish ,  new connection entry in forwarding table , Connection is released, entry removed from table. 	| No VC setup Each time end system when sends a packet It stampas packet with destination(end system) address Maintain info in forwarding table 	|
| Light headed                                                                                                                                      	| Over headed                                                                                                                                   	|
| **signaling protocols:** Message protocol for - sending initiating and terminate message to setup VC.                                             	| When packet arrives at router it uses , packet’s destination address to forward packet                                                        	|
| Determine the path(_series of links and routers_) between sender and receiver.                                                                    	| **longest Prefix matching algorithm** is used with destination address in a router to find the link interface                                 	|
| Determine VC number for each link along the path                                                                                                  	| **NO connection state information** is stored                                                                                                 	|
| Reserve network resources (bandwidth)along the path                                                                                               	| Resources are on-demand                                                                                                                       	|
| Packet flow the same path                                                                                                                         	| Different packets may flow different paths                                                                                                    	|
| Packets Arrives in order                                                                                                                          	| Packets arrive out of order                                                                                                                   	|
| Less Delay                                                                                                                                        	| More Delay                                                                                                                                    	|
| Eg : ATM ( Asynchronous transfer mode)                                                                                                            	| Eg : Internet                                                                                                                                 	|


_Note : connection oriented service in transport layer different from network layer connection system_
 




