# Network Fundamentals Day 1

For my first day in the blog I will be starting with learning Networking Fundamentals using TryhackMe. My goal is to brush up on my knowledge of networking and to begin working towards obtaining the CompTIA Network + Certificate. Here we go :point_down:

What is a ***network***? A network is a group of devices that are interconnected with each other to allow for communication.

What is the ***internet***? The internet is a massive singular network that is comprised of small networks working together. The small networks making up the internet is what we call ***private networks*** while the networks that connect all of these private networks are called ***public networks***. 

All devices have two main ways of getting identified on a network:
1. Your ***IP Address*** (Internet Protocol)
2. Your ***MAC Address*** (Media Access Control Address)

## IP Addresses

The IP Address is a chain of numbers that are divided into ***four octets***. Each of the numbers of the octets are calculated using something called ***IP addressing*** and ***subnetting***. The IP address of a device can change but there cannot be duplicate IP addresses in the same network. 

IP addresses follow certain ***protocols*** that allow devices to communicate among one another. Devices can have private and public IP addresses. A public IP address is what we use to find the device on the internet while a private address is used to find a device in a pool of other devices. 

For example: when you have two devices on a private network, they will use their private IP addresses in order to talk to each other but when they send data to the internet, they will use their public IP address. Your device obtains the public IP address from your ***Internet Service Provider***.

As the number of devices connected to the internet increases yearly, our current addressing scheme ***IPv4*** becomes obsolete which has led to the development of the ***IPv6***. This new addressing scheme can hold more combinations of IP addresses but it runs into the problem of having a much longer address. 

## MAC Addresses

When a device is manufactured it comes built with a ***physical network interface***, which is a microchip board that is on the motherboard. The network interface is given a special address also know as a MAC address. MAC adresses are made out of twelve hexadecimal characters that are split into two's and divided by colons (seperators). The first six characters of the MAC address are represented by the vendor who manfuactured the device while the last six are unique to the device itself.

What is ***spoofing***: spoofing is the practice of having a foreign device pretend to be another device by using its MAC address. This can lead to the hacker breaking poor security designs and exploiting vulnerabilities. 