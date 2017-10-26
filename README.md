# CS118-Proj2

Developers: Michelle Tran and Shannon Tom 

UCLA Computer Science 118, Computer Networks Fundamentals
Winter 2017
Project 2

Implementing Window-based Reliable Data Transfer Protocol

We tried to mimick the Selective Repeat TCP protocol by building a simple window-based protocol with timers over UDP sockets. 
The project entailed of building a server program that listened for requests and sent out packets of the requested file, with 
timers on each packet (using the select() function). 

The client program would send out a SYN packet to attempt to connect to the server before requesting a file. After that, it will send out ACK packets for each packet that it has received. The client also maintains a timer for each ACK packet and resends the packet if the timer goes off. 

The timers are restarted once both programs receive acknowledgements of receipt. 
