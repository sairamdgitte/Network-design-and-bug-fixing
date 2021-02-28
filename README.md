# Network-design-and-bug-fixing
Network design and bug fixing on CORE simulator network. Tasks that were delivered successfully: Setting up static routing tables, Fixing bugs in the entire network, Setting up a gateway router and adding default routes, Adding a new DHCP router with extra subnets to the existing network, Implementing a Demilitarized Zone by implementing a firewall on the gateway router, protecting company's web server from remote-login (secure shell) Tools used: CORE simulator


# Tasks

1. Setting up static routing tables in all four routers such that the three networks
containing computers (the clients, the www server, and the intranet
server) can reach each other. Take into account the link speeds between
the routers, to find routes that deliver good speed and latency (you are
not allowed to change the link speeds).

2. Finding three errors in the network configuration. All errors are in either the
configuration of the IP addresses and masks and/or the static routing
tables. For each error, describe what the problem is, how you found it,
the fix you applied, and how you can test that the fix works.
After fixing the errors, you should be able to execute the command
lynx www.fit9137 successfully. 

3. The network currently has no gateway to the Internet. We want to make
router R3 the gateway router. Add default routes to all other routers such
that any packet whose destination is outside of the company network is
routed via R3.

4. Adding a new subnet with 4 clients that are connected to the existing
network using a new router. The subnet is allocated the network address
192.168.200.0/24.
The new router should be named External. It connects to the gateway
router R3 and should be configured with a default route to R3. To get full
marks, the clients need to be configured with DHCP, i.e., the new
External router must be running a DHCP server. You can use router R1
and the clients in its subnet as an example of how to set up DHCP. 

5. The server with the label www acts as the company’s public web server,
and the server with the label ssh as the remote-login (secure shell)
server. The company decided to update its security policy and implement
a Demilitarised Zone (DMZ). Your task is to implement a firewall on
router R3 such that:
a. Any packets for the specific servers in the DMZ are accepted
(HTTP packets for www, SSH packets for ssh, and DNS packets
for dnsserver), as well as any ICMP packets for devices in the
DMZ.
b. Any packets from inside the company network are accepted.
c. Any packets relating to connections that were established from
inside the company network are accepted.
d. Any SSH packets from the ssh server into the company network
are accepted.
e. Any other packets are blocked.


