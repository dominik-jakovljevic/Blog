# Network Fundamentals Day 3

## Introduction to LAN Continued 

What is the ***ARP Protocol***? The ARP Protocol also known as the Address Resolution Protocol, is the protocol that gives devices the ability to identify themselves on a network. In other words, it lets the devices to associate its own MAC address with an IP address inside of the network. All the other devices on the network will keep track of what MAC addresses belong to what devices. Devices use the ARP protocol to find other devices on a network. 

Every single device on a network has a place to store data also known as a ***cache***. This cache will store the different identifiers of all the other devices in the network. The two identifiers that have to be stored are of course the IP addresses and MAC addresses of all the devices. The ARP protocol sends two types of requests in order to identify the two. It sends a ***ARP Request*** and an ***ARP Reply***. 

When the ARP Request is sent out, it messages all the other devices and asks them if devices MAC address matches the IP address that was requested. When the device with the requested IP address is found, an ARP Reply comes back to the original device. 

What is the ***DHCP Protocol***? There are two ways that a device can obtain an IP address, one way is by manually entering them into the device and the other way is by using a DHCP server or Dynamic Host Configuration Protocol server. Whenever a devices enters a network if it hasn't obtained an IP address yet, it sends out a request or ***DHCP Discover*** to find out if there are DHCP servers in the network. Next the DHCP server reponds with an IP address for the device or what we call ***DHCP Offer***. When the device gets this, it sends out a confirmation that it wants the IP address (***DHCP Request***). Finally the server tells the device that the IP address can be used (***DHCP ACK***).

## OSI Model

What is the ***OSI Model***? The OSI Model which stands for Open Systems Interconnection Model is the most fundamental model used in the networking world. The model is an example for how networking devices shall send/receive and interpret information. One of the biggest advantages of using the OSI Model is that it allows all devices on a network no matter what type of device to talk with all the other devices. The OSI model contains seven distinct layers starting from 7 and going down to 1. The OSI model uses the process of ***encapsulation*** to add additional pieces of data as the data moves through each distinct layer of the model. 

Layers of the OSI Model:

1. ***Physical***: this layer is where all of the physical parts and hardware of networking are found. These devices incorporate electrical signals to send data to other devices using binary. An example of these types of devices are ethernet cables. 

2. ***Data Link***: this layer is whats responsible for the physical addressing of transmissions. What happens is it obtains a packet coming from the network layer along with its IP address and puts in the MAC address of the endpoint device. In every device that is network-enabled, you can find a ***Network Interface Card*** which has its own MAC address. The MAC address is made by the manufacturer of the device and cannot be changed or altered but it can be spoofed (stolen). Another job of this layer is to make the data into a suitable format for transmission. 

3. ***Network***: this layer is where the small packets sent are reconstructed back into big pieces of data. This is done through the use of ***routing*** and ***re-assembly***. Routing is the optimal path in which the packets should be sent. The factors that determine what's the most optimal path for the data to take include:

    * Which path has the least amount of devices that the packets need to travel (shortest path)

    * Which path has the most reliability

    * Which path has the fastest connection

    Devices that deal with IP addresses such as routers are known as Layer 3 devices since they work in this layer of the OSI Model. 

4. ***Transport***: this layer of the model is responsible for sending data across the entire network. When the data is sent, it is sent by one of two protocols depending on a few circumstances. These protocals are called ***TCP (Transmission Control Protocol)*** and ***UDP (User Datagram Protocol)***. The TCP's purpose is to hold a steady connection between the two devices for the whole duration of the data transfer. TCP also has a feature called error checking that enables the protocol to make sure that the data that was sent in small chunks to another device was reassembled in the same order. 

    TCP is used primarily for things like file sharing, sending emails, and browsing the internet. TCP is used in these situations to make sure that the data is complete. 

    Below is a table of the advantages and disadvantages of TCP: :point_down:

    | Advantages  | Disadvantages |
    | ----------- | ------------- |
    | Accurate Data | If one chunk of data is missing, the data cannot be used |
    | Prevents the flooding of data by synching devices | Slow connection speeds can bottleneck other devices |
    | Is more reliable | TCP is slower than UDP because the decives have to do more things under the TCP protocol |

    On the other side of the spectrum, UDP is not as advanced or sophisticated as TCP. Any and all data that is sent using UDP is sent to the other device no matter if it actually gets there or not. UDP just hopes that all of the data is sent properly without any checking. UDP is mainly used when small packets are sent from device to device. 

    Below is a table of the advantages and disadvantages of UDP: :point_down:

    | Advantages | Disadvantages |
    | ---------- | ------------- |
    | A lot faster than TCP | UDP doesn't care if the data was received or not |
    | It leaves the application layer to decide how fast to send packets of data | It is flexible for developers which means they can overwrite rules and protocols |
    | It does not need a stable connection to work | Bad connections make a bad user experience |

5. ***Session***: when the data has been correctly translated from the Presentation layer, this layer will start to create a connection to the device that the data is meant for. When the connection is established, a session is also created. This layer makes sure that the two devices are synchronised before data is transfered. When everything is working well, this layer will break up the data into small packets and then send them all at once. 

6. ***Presentation***: this layer is responsible for translating data that comes to and from the Application layer. It makes sure that the data obtained looks the same no matter what device it is viewed on. Also, this layer of the model is where you can find the HTTPS protocol which is important for data encryption.

7. ***Application***: this is the layer of the model that you are most familiar with. This layer is where you as the user interact with the data. This is done through having the proper protocols and rules in place. This is most commonly done with a ***Graphical User Interface*** or GUI such as Microsoft Windows. This layer is also where the ***Domain Name System*** protocol is found which is responsible for converting website url's into IP addresses. 
