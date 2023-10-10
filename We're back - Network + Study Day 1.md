# We're Back - Network Plus Study Day 1

## OSI Model Walkthrough

What does the ***OSI Model stand for?*** It stands for Open Systems Interconnection Reference Model

The ***OSI Model*** is a model or guide, it's not a law in the world of computing

When the ***OSI Model*** was first concieved, they wanted to implement the OSI protocol suite. But instead they went for TCP / IP

For every layer in the ***OSI Model***, there are sets of protocols that are used to make sure that the layers are operational

A common acronym for the ***OSI Model*** is: All people seem to need data processing 

### Layer 1 (Physical Layer) of the OSI Model

***Layer 1*** of the OSI Model is called the ***physical layer***

This layer is where we can find all of the cables, connectors, and signaling. One thing that this layer isn't about is about protocols. 

When there is a problem on the ***physical layer*** it means that the cabling should be fixed, loopback tests should be ran, and swap adapter cards

### Layer 2 (Data Link) of the OSI Model

***Layer 2*** of the OSI Model is called the ***Data Link layer***

We can find the foundation of the communication at this layer

The protocols that run at ***layer 2*** are called Data Link Control (DLC) protocols and they include:

- MAC (Media Access Control) address on Ethernet

Sometimes we call ***layer 2*** the switching layer

### Layer 3 (Network) of the OSI Model

***Layer 3*** of the OSI Model is called the ***network layer*** or even the routing layer

This is the layer that works with IP (internet protocol)
addresses

Frames are fragmented (broken into smaller pieces)
at ***layer 3***

### Layer 4 (Transport) of the OSI Model

***Layer 4*** of the OSI Model is called the ***transport layer*** 

Sometimes we called ***layer 4*** the post office layer because it determines how and where the data will be delivered 

The protocols that are used at ***layer 4*** include:

- TCP (Transmission Control Protocol)
- UDP (User Datagram Protocol)

### Layer 5 (Session) of the OSI Model

***Layer 5*** of the OSI Model is called the ***session layer***

This is where communication management between devices happens such as start, stop, and restart

### Layer 6 (Presentation) of the OSI Model

***Layer 6*** of the OSI model is called the ***presentation layer***

***Layer 6*** is where character encoding and application encryption take place 

This layer is often combined with layer 7 so we can actually use the applications 

### Layer 7 (Application) of the OSI Model

***Layer 7*** of the OSI model is called the ***application layer***

This layer is what we see on our computers. For example the google page runs on ***layer 7***

### Example

An example of all of these layers in action is when we used an application such as Gmail:

1. Physical: Electrical signals
2. Data Link: Ethernet
3. Network: IP encapsulation
4. Transport: TCP encapsulation
5. Session: Link the presentation to the transport
6. Presentation: SSL encryption
7. Application: https://gmail.com

## Data Communication

### Protocol Data Unit (PDU)

***Protocol Data Units (PDU)*** or transmission units is what is used to move data from one part of the network to another

Ethernet operates on a frame of data which means that it doesn't care what's on the inside, its only job is to send it to another device

IP operates on a packet of data which means that it finds either TCP or UDP inside but it doesn't care which

When it's TCP it's called a TCP segment but when it's UDP it's called a UDP datagram

Here is an example of how this works:

Layers 5, 6, 7 - Application Data

Layer 4 - TCP Header, Application Data

Layer 3 - IP Header, TCP Header, Application Data

Layer 2 - Frame Header, IP Header, TCP Header, Application Data, Frame Trailer

### TCP Flags

The header describes or identifies the payload
aka. here's what you're about to see

The TCP header has important control information and includes a set of bits called ***TCP flags***

These flags control the payload with these set of messages:

- SYN - Synchronize sequence numbers
- PSH - Push the data to the application without buffering 
- RST - Reset the connection
- FIN - This signals the last packet from the sender

### Maximum Transmission Unit (MTU)

The ***maximum transmission unit*** is what we call a maximum IP packet to transmit without fragmenting it 

The reason we avoid fragmentation is because it slows things down. When we lose a fragment we lose an entire packet of data and it requires a lot overhead along the path

It is difficult to know the ***MTU*** all the way through the path. The automated methods are innacurate especially when you filter ICMP

### Building an Ethernet frame

TCP Header | TCP Data

TCP Header | TCP Data | IP Header

DLC Header | TCP Header | TCP Data | IP Header | FCS

The maximum IP packet size you can send using ethernet is 1500 bytes

### MTU Troubleshooting

***MTU*** sizes are usually configured once. This is based on network infrastructure and don't change very often

These sizes are a concern for tunneled traffic. The tunnel could be smaller than your local Ethernet segment

What happens when you send packets with Don't Fragement (DF) set? When this happens the routers will respond back and tell you to fragment and at this point it is likely you will get the ICMP message.

You can troubleshoot using the ping command. 

You can ping to Google's DNS servers using this command on the mac terminal:

    ping -D -s 1472 8.8.8.8

Or this when you are on windows:

    ping -f -l 1472 8.8.8.8

This way you can see if your MTU is configured to the appropriate size

## Network Topologies

***Network Topologies*** are useful in planning new networks such as the physical layouts of buildings and they assist in understanding signal flow 

One of the most popular types of topologies is the ***star topology*** or sometimes called the hub topology. These are used in a lot of small and large networks and it connects all the devices to a single central device. The switch in the middle is connected to all of the devices in the network

Another type of topology is called the ***ring topology***. It is mainly used in Metro Area Netowrks and Wide Area Networks. 

The third type of topology is called the ***bus topology***. These were early local area networks that where the devices were connected by a coaxial cable. It is a simple topology but it is really prone to errors. If only one part breaks, the entire network is shut. 

A really popular topology that is used in larger networks is the ***mesh topology***. Each device has multiple links to the same place. These are mostly used in the wide area networks (WANs).

A really common type of topology is what we call a ***hybrid topology***. Most modern day networks are hybrid topologies which means they are a mix of the topologies above.

## Network Types

### P2P Networks

In a ***Peer to Peer Network***, there are no servers or clients rather every device is a server and client. Everyone is talking to everybody

Some advantages of this type of network is that they are really easy to deploy and they are low in cost

Some disadvantages are that they are difficult to administer and difficult to secure

### Client-Server

In a ***client server***, there is a central server where the clients talk to the server. None of the clients talk to each other

Some advantages of this type of network include higher performance and easy to administer

Some disadvantages of this type of network are that it costs a lot and that it is really complex

### Local Area Network (LAN)

A Local Area Network is relative. They usually are in the buildings in which you are in right now and provide the building with high speed connectivity. This is usually done through ethernet cables

### Metropolitan Area Network (MAN)

The ***MAN*** is used as a network in your city. These types of networks are larger than LAN's but smaller than WAN's

It's very common for governments to use ***MAN*** because of how dispersed government offices can be

### Wide Area Network (WAN)

These types of networks span the globe. ***WAN*** connects LAN that spane long distances. But ***WAN*** is slower than LAN connectivity.

### Wireless Local Area Network (WLAN)

These types of networks are usually used in buildings and geographically remote locations

It is possible to expand the coverage of a ***WLAN*** but adding additional access points

### Personal Area Network (PAN)

These types of networks are used in our everyday lives. Examples of these type of networks are mobile hotpsots, bluetooth, and wireless technology

### Campus Area Network (CAN)

These types of networks are used primarily in college campuses, medical hospitals, and just any group of buildings that need to share the same information. These achieve this using high speed Ethernet

## NAS vs SAN

### NAS

***NAS*** which also stands for ***Network Attached Storage*** is a type of storage that is connected to a shared storage device across a network and gives you file-level access.

This means that if you want to overide just 1 MB in 1 GB of storage that you will have to overide the whole 1 GB

### SAN

***SAN*** which also stands for ***Storage Area Network*** is a type of storage that feels like a local storage device. It is very efficient in reading and writing data

One thing that they both have in common is that they both require a lot of bandwidth. Both also may use isolated networks and high-speed network technologies



