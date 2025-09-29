
2025-09-28 14:45

Level : 

Tags : [[networking]], [[linux]]

# networking-fundamentals

## The OSI (Open Systems Interconnection) Model
- The osi model is a conceptual framework that describes seven distinct layers of network communication. It  helps us to understand how different technologies work together to enable a network.
- Its basically a set of rules that explains how different computer systems communicate over a network.
- It consists of 7 layers and each layer has specific functions and responsibilities
### Layer 1 : Physical Layer

- The lowest layer of the OSI model
- Responsible for the actual physical connection between devices
- Contains information in the form of bits and transmits them from one node to the next (0s and 1s)
- When receiving data, this layer will get the signal received and convert it to 0s and 1s and send them to the DLL
- Common physical layer devices are hub, repeater and cables
- Physical layer specifies how the different devices are arranged in a network i.e. bus topology, star topology or mesh topology
- This layer also defines how the data flows between two connected devices e.g simples, half duplex and full duplex
### Layer 2 : Data Link Layer (DLL)

- Responsible for the node to node delivery of the message
- The main function is to make sure data transfer is error-free from one node to another over the physical layer
- When a packet arrives in a network, it is the responsiblity of the DLL to transmit it to the host using its MAC address.
- Switches and bridges are the common DLL devices
-  Packet in the DLL is referred to as Frame
- DLL also encapsulates the sender's and receiver's MAC address in the header 
### Layer 3 : Network Layer

- The network layer is responsible for the transmission of data from one host to the other located in different networks. 
- It also takes care of packet routing i.e. selection of the shortest path to transmit the packet from the number of routes available
- The sender's and receiver's IP address are placed in the header by the network layer
- Network layer is implemented by networking devices such as routers and switches
- Protocols - IP(Internet Protocol), ICMP (Internet Control Message Protocol)
### Layer 4 : Transport Layer
- The transport layer provides services to the application layer and takes services from the network layer. The data in this layer is referred to as Segments
- It is responsible for the end to end delivery of the complete message
- It also adds source and destination port number in its header
- Protocols - TCP (Transmission Control Protocol), UDP (User Datagram Protocol)
### Layer 5 : Session Layer
- This layer is responsible for the establishment of connections, management of connections, termination of sessions between 2 devices. It also provides authentication and security
### Layer 6 : Presentation Layer
- Also called the translation layer. The data from the application layer is extracted here and manipulated as per the required format to transmit over the network.
- Protocols used here are TLS/SSL
### Layer 7 : Application Layer
- Provides the interface for applications to access network services.
- Protocols: HTTP, HTTPS, FTP, SMTP, DNS

### Analogy
- Step 1: Person A interacts with e-mail application like Gmail, outlook, etc. Writes his email to send. (This happens at Application Layer).
- Step 2: At Presentation Layer,Mail application prepares for data transmission like encrypting data and formatting it for transmission.
- Step 3: At Session Layer there is a connection established between the sender and receiver on the internet.
- Step 4: At Transport Layer, Email data is broken into smaller segments. It adds sequence number and error-checking information to maintain the reliability of the information.
- Step 5: At Network Layer, addressing of packets is done in order to find the best route for transfer.
- Step 6: At Data Link Layer, data packets are encapsulated into frames, then MAC address is added for local devices and then it checks for error using error detection.
- Step 7: At Physical Layer, Frames are transmitted in the form of electrical/ optical signals over a physical network medium like ethernet cable or WiFi.






## References
1. https://www.geeksforgeeks.org/computer-networks/open-systems-interconnection-model-osi/