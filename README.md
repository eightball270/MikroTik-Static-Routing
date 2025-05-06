# MikroTik Static Routing
Similar to static routing configuration on [Cisco](https://github.com/eightball270/CodingStudio-ComputerNetworkFundamentals?tab=readme-ov-file#static-routing) devices, MikroTik routers also require static routing to be configured on each router by manually creating a routing table. This configuration involves specifying the destination network address and its corresponding gateway.

## Technology Used
- GNS3

## Requirements
1. 6 Client PCs
2. 3 Routers and Swithces
3. Straight-Through Cables
4. Crossover Cables (for inter-router connection)

## Configuration Done
1. The IP address on the router is used as the gateway for each client PC and for the inter-router network
2. Static IP address of each client PCs
3. Static routing configuration via command-line

## Static Routing
On a MikroTik router, a routing table is formed by adding the destination network address (dst-address) and its corresponding gateway. For example, to allow a client directly connected to Router R2 to access the 192.168.10.0/24 network, configure static routing on Router R2 with dst-address 192.168.10.0/24 and use the IP address of Router R1 (10.10.10.1), which is directly connected to Router R2, as the gateway. The command-line format on MikroTik is:  
`[admin@MikroTik] > ip route add dst-address=192.168.10.0/24 gateway=10.10.10.1`  

![Static Routing (MikroTik).png](https://github.com/eightball270/MikroTik-Static-Routing/blob/main/Static%20Routing%20(MikroTik).png)

[Project File Link](https://github.com/eightball270/MikroTik-Static-Routing/blob/main/Static%20Routing%20(MikroTik).gns3project.rar) (extract the file first)

Traceroute from PC2 (192.168.10.3/24) to PC3 (192.168.20.2/24) and PC6 (192.168.30.3/24) :

![Static Routing (MikroTik) (1).png](https://github.com/eightball270/MikroTik-Static-Routing/blob/main/Static%20Routing%20(MikroTik)%20(1).png)
