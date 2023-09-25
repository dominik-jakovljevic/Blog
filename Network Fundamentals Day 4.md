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

