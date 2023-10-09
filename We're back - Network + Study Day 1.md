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


