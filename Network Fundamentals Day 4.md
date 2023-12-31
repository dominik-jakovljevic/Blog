# Network Fundamentals Day 4

## Packets & Frames

What are packets and frames? In simple terms, packets and frames are small chunks of data when put together form a large piece of data that contains readable information. ***Frames*** can be found in layer 2 of the OSI model (Data Link) which means they don't deal with IP addresses. One way to think about frames is like a pair of Russian dolls. Inside of the bigger doll, you will find one smaller one. Frames are similar to this because inside of the first doll (the packet) is another smaller doll (frame) that contains data. This concept is called ***encapsulation***. 

But, when we talk about IP addresses getting involved we are usually talking about ***packets***. Packets are used to communicate data across multiple networking devices. Since packets are small pieces of data, the chance for bottlenecking in the network is reduced. 

One example of this is when you send a large picture across a network. You would think that the image is sent as one but you would be wrong. It is actually sent in small packets and then reassembled at the destination. 

## TCP / IP (3-Way Handshake)

***Transmission Control Protocol (TCP)*** is another rule that we using in networking. One cool thing about this certain protocol is that it is similar to the OSI model. This protocol contains 4 layers and seen as a simplified version of the OSI model.

The 4 layers are: 

* Application
* Transport
* Internet
* Network Interface

Much like how the OSI model works, data is added to each layer of the protocol which is the process of encapsulation. One of the biggest featuress of the TCP protocol is that it is connection-based which means that the protocol needs to establish a connection from the origin device to another in order for data to be sent. This feature is what guarantee's data to be recieved on the other side which is what we call the ***Three-way handshake***.

Below is a table with the advantages and disadvantages of TCP: :point_down:


| Advantages | Disadvantages |
| ---------- | ------------- |
| Data has integrity | It needs a constant reliable connection in order to transfer data. If the connection times out even once, the data is corrupted |
| It can synch devices to prevent data flooding in the wrong order| Having a slow connection can bottleneck the other device on the network |
| Is reliable | TCP is a lot slower than UDP |

Additionally, TCP packets have ***headers*** that were added onto them during encapsulation. This is done in order to add additional pieces of data to the packets.

In order to create a connection between devices, something called the Three-way handshake has to happen. This is done by using special messages.

A table of the special messages is below: :point_down:

| Step | Message | Description |
| ---- | ------- | ----------- |
| 1    | SYN     | Initial packet sent by client. Is used to make the first connection and synch devices |
| 2    | SYN / ACK | Packet sent from the receiving device to confirm the synch from the client |
| 3    | ACK     | Acknowledgement packet that is used by either client or server to acknowledge that packets have been recieved |
| 4    | DATA    | When a connection is established, data is sent |
| 5    | FIN     | Once the connection is finished, it is then closed properly |
| #    | RST     | This packet ends all communication. This indicates there was a problem somewhere |

The data that gets sent through the network is given a number sequence that is random and is reconstructed at the end by using the number sequence and by incrementing by 1. One caviat is that both computers on the network have to agree on the same number sequence for the data. 

Also, in order for TCP to close a connection, it has to determine that the receiving device has got all of its data. Since TCP has reserved system resources on all devices, it is a good idea to turn it off once it is done doing its job. 

## UDP / IP

Another protocol that we use when communicating between devices is the ***User Datagram Protocol (UDP)***. One great thing about UDP is that it doesn't require a constant connection between devices for the data to travel. Because of this, the Three-way handshake does not happen. 

Below is a table of the advantages and disadvantages of using UDP: :point_down:

| Advantages | Disadvantages |
| ---------- | ------------- |
| Much faster than TCP | UDP doesn't check if the data has been recieved or not |
| UDP gives the application layer the ability to decide how quickly packets will be sent out | It lets developers bend the rules of the protocol |
| A constant connection is not needed | Bad connections result in a bad user experience |

The UDP protocol and the packets that comes from the protocol are a lot simpler than TCP packets. One thing that these two protocols have in common is that they both share some similar headers. 

Below is a table of the headers that both protocols share: :point_down:

| Header | Description |
| ------ | ----------- |
| Time to Live (TTL) | Sets an expiration for the packet. If it doesn't reach its intended destination it will be removed so it doesn't slow down the network. |
| Source Address | IP address of the device where the packet is coming from |
| Destination Address | IP address of the device where the packing is going to |
| Source Port | The port that is opended by the device sending data in order to send the UDP packet. This port value is random |
| Destination Port | The port number that the application or service is running on the remote host. An example of this would be a server running on a specific port. This port number is not chosen at randmom. |
| Data | The header where the data of a file is stored |

## Ports

What is a ***port***? Networking devices use ports in order to enforce strict rules when talking to each other. Once the connection is made, all the data coming to and from the device will be traveling through these ports. Ports can be numbered anywhere from 0 to 65535. Because of these wide range of numbers it becomes tough to keep track of all the applications and which ports they are running through. One way we mitigate any confusion is by assigning certain applications to certain ports. For example, web browsers run on port 80. This means that all of the data for the web browsers will be coming through port 80. All ports that are between 0-1024 are what we call ***common ports***.

Below is a table of certain protocols and which ports they run on: :point_down:

| Protocol | Port Number | Description |
| -------- | ----------- | ----------- |
| File Transfer Protocol (FTP) | 21 | This protocol is used for downloading files from a central location |
| Secure Shell (SSH) | 22 | This protocol is used to login to different systems through a secure text-based system |
| HyerText Transfer Protocol (HTTP) | 80 | This protocol is used to power the internet. Browsers use this to download text, images, and videos of web pages |
| HyperText Transfer Protocol Secure (HTTPS) | 443 | This protocol has the same purpose as HTTP but it instead uses secure encryption algorithms |
|Server Message Block (SMB) | 445 | This protocol is very similar to FTP but it also allows you to share different devices |
| Remote Desktop Protocol (RDP) | 3389 | This protocol is used to securely login to a system using a visual desktop interface |

