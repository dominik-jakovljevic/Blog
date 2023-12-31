# Network Fundamentals Day 2

## Ping

What is ***Ping***? Ping is an essential networking tool that security professionals rely on to determine if the connection between devices exists or is reliable. Ping does this using the ***Internet Control Message Protocol*** (ICMP). Ping calculates the connection speed between devices by tracking how long it takes for ICMP packets to travel for one device to another. The calculations are done using ICMP's echo packet and echo reply from the device. 

You can ping pretty much everything that is connected to a network such as different websites or even your own network at home. 

The proper syntax in order to use the ping tool is:

    ping IP address 

And if you don't know the IP address:

    ping website url

## Introduction to LAN

What is ***network topology***? Network topology is quite literally the way that the network is designed and how it looks. 

Types of network topologies:

1. ***Ring topology***: this is where all the devices on a network such as computers are connected by cable to form a loop. Data in this type of topology is sent until it reaches the device it was meant for. Since the data travels all in one direction and in an continoued loop, it is pretty easy to find any bugs that might arise. But also since the topology depends on the other devices in the network to relay data, if anything happens to the cable or devices the entire network will break making it obsolete. 

2. ***Bus topology***: this is where all the devices on a network are connected by a single cable called the ***backbone cable***. Since all of the devices are connected and branch out (like leaves on a tree) from a single cable, the data quickly becomes slow to reach the desination devices (this is what we call ***bottlenecking***). When a bottleneck occurs, it becomes hard to troubleshoot where the problem is coming from since all the data is traveling along the same route. One positive about this topology is that it is easier to set up than the others and usually cheaper to set up. Much like the Ring topology, if anything happens to the backbone cable, the entire network will break. 

3. ***Star topology***: The idea behind this type of topology is that all of the devices on the network are connected by one central switch/hub. This topology is by far the most common today because of it's reliability and efficiency. All data sent to a device in the network is sent from the central device in the network such as a switch. One disadvantage of this topology is that it becomes expensive because of all the cabling and networking equipment needed. But one of the biggest advantages to this topology is that it is extremely scalable. You can add additional devices at any time with ease. But this also comes with a drawback, with more and more devices on the network it means that you have to spend more time maintaining the network as a whole. If the switch in the center fails, it cuts connection to all of the devices and breaks the entire network. 

## Switch

What is a ***switch***? A switch is a special device in a network that is made to connect multiple networking-capable devices via ***ethernet***. To do this you plug the devices into the ports of a switch. Switches are mainly used in larger networks where large numbers of devices can be found. The switch has ports numbered 4, 8, 16, 24, 32, 64 which is used for devices to plug into and connect to a larger network. One useful thing that switches do is keep track of what device is connected to which port. This allows for the switch to send data straight to the desired device instead of sending it to all of the devices on the network. 

Routers and switches can be also connected to each other. When you do this, it increases the ***redundancy*** (reliability) of the network by allowing the data to flow through different paths. When one path gets cut, the data can flow through the other which means there is no downtime when something goes wrong. 

## Router

Nice and simple, a router is used to connect different networks and allow data to travel between them. It does this by creating a path between the networks so the data can travel between.