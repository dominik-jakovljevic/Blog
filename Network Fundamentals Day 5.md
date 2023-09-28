# Network Fundamentals Day 5

## Port Forwarding

What is ***port forwarding***? Port forwarding is what's responsible for connection services and applications on your network to the Internet. If port forwarding didn't exist, all of the services and networks would only work in one network instead of the whole internet. Port forwarding opens specific ports which enables the data to flow through multiple networks instead of one.

The device that is used to enable port forwarding is the router.

## Firewalls

What is a ***firewall***? A firewall is a device than can be found in a network and its job is to determine what sort of traffic will be allowed to enter or exit.  A network administrator can set the firewall to ***permit*** or ***deny*** traffic entering or exiting the networking depending on certain factors. 

The factors are: :point_down:

* Origin of the traffic (the firewall could be directed to accept or deny traffic coming from certain networks)
* The destination of the traffic (the firewall could be directed to accept or deny traffic going to a certain network)
* Which port is the traffic for 
* The protocol that the traffic is using

In order to answer the questions above :point_up: , firewalls have to perform packet inspection.

How the firewall can look like depends on factors such as how large the networks are and how many users they are supporting. For example, a firewall that is supporting a large business with a lot of users can be a dedicated piece of hardware. But, there is also software such as Snort that can work as a firewall for smaller networks with fewer users. One thing that applies to all firewalls is that they can be categorised into 2-5 categories. 

A table with the two biggest categories of firewalls is below: :point_down:

| Firewall Category | Description |
| ----------------- | ----------- |
| Stateful          | Stateful firewalls use all of the data from the connection instead of looking at individual packets. It decides the devices behavior depending on the entire connection. This type of firewall also uses up a lot more resources than other types. Also, if the connection from the host isn't reliable, the device will be blocked |
| Stateless         | Stateless firewalls use certain rules to determine if individual packets should be accepted or not. If a device sends a bad packet it won't shut the entire device out of the network. These types of firewalls do use less resources but that also means that they are much dumber. Also, these types of firewalls are good when you are getting big amounts traffic from a set of hosts |

## VPN (Virtual Private Network)

What is a ***VPN***?



