# MikroTik Static Routing
Just like configuring static routing on [Cisco](https://github.com/eightball270/CodingStudio-ComputerNetworkFundamentals?tab=readme-ov-file#static-routing) devices, MikroTik routers also require static routing to be configured on each router by manually creating a routing table. To create a routing table, you need to enter the destination network address and its corresponding gateway.

## Technology Used
- GNS3

## Requirements
1. 12 Client PCs
2. 3 Routers and Swithces (divided 2 VLANs)
3. Straight-Through Cables
4. Crossover Cables (for inter-router connection)

## Configuration Completed
1. VLANs on routers and switches
2. The IP address on the router is used as the gateway for each client PC and for the inter-router network
3. Static IP address of each client PCs
4. Static routing configuration via command-line

## Static Routing
On a MikroTik router, a routing table is formed by adding the destination network address (dst-address) and its corresponding gateway. For example, to allow a client directly connected to Router R2 to access the 192.168.10.0/25 network, configure static routing on Router R2 with dst-address 192.168.10.0/25 and use the IP address of Router R1 (10.10.10.1), which is directly connected to Router R2, as the gateway. The command-line format on MikroTik is "ip route add dst-address=192.168.10.0/25 gateway=10.10.10.1".

![Static Routing (MikroTik)](https://github.com/eightball270/MikroTik-Static-Routing/blob/main/Static%20Routing%20(MikroTik).png)

[Project File Link](https://github.com/eightball270/MikroTik-Static-Routing/blob/main/Static%20Routing%20(MikroTik).gns3project.7z)

Traceroute from PC12 (192.168.30.131/25) to PC6 (192.168.20.3/25) and PC1 (192.168.10.2/25) :

![Static Routing (MikroTik) (1)](https://github.com/eightball270/MikroTik-Static-Routing/blob/main/Static%20Routing%20(MikroTik)%20(1).png)

