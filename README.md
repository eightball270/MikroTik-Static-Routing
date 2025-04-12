# MikroTik-Static-Routing
Just like configuring static routing on [Cisco](https://github.com/eightball270/CodingStudio-ComputerNetworkFundamentals?tab=readme-ov-file#static-routing), MikroTik routers must also configure static routing on each router by manually creating a routing table. The configuration of creating a routing table is to enter the destination network address and its gateway.

## Technology Used
- GNS3

## Requirements
1. 12 Client PCs
2. 3 Routers and Swithces (divided 2 VLANs)
3. Straight-Through Cables
4. Crossover Cables (for inter-router connection)

## Configuration Completed
1. VLAN on routers and switches
2. IP address on the router which is used as the gateway for each client PCs and inter-router network
3. Static IP address of each client PCs
4. Static routing configuration via command-line

## Static Routing
In a Mikrotik router, form a routing table by adding the destination network address (dst-address) and its gateway, for example so that a client directly connected to router R2 can connect to network address 192.168.10.0/25, then configure router R2 static routing with dst-address 192.168.10.0/25 with router R1's ip address directly connected to router R2 (10.10.10.1) as the gateway. The command-line format on Mikrotik is "ip route add dst-address=192.168.10.0/25 gateway=10.10.10.1".

![Static Routing (MikroTik)](https://github.com/eightball270/MikroTik-Static-Routing/blob/main/Static%20Routing%20(MikroTik).png)

Traceroute from PC12 (192.168.30.131/25) to PC6 (192.168.20.3/25) and PC1 (192.168.10.2/25) :

![Static Routing (MikroTik) (1)](https://github.com/eightball270/MikroTik-Static-Routing/blob/main/Static%20Routing%20(MikroTik)%20(1).png)

