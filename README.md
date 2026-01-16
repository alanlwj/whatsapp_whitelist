# whatsapp_whitelist
# To be stringent with your firewall rules it always to block any-any in outgoing rules instead of allowing all and there are alot of testing needed to be done. I am creating this rules for everyone and hope to continuously update this to ensure we can allow Whatsapp in the network with stringent firewall rules.

1) Create TCP Port Alias: Whatsapp_TCP(80, 443, 5222, 5223, 5228)
2) Create UDP Port Alias: Whatsapp_UDP(3478, 45395)
3) Create UDP/TCP Port Alias: Whatsapp_TCPUDP (3478, 45395) - This is crucial for Phone Call else the call may time-out or even if the call is pickup there will be no transmission!
4) Create list of Facebook IPv4: Whatsapp_IPv4 - Refer to the ip list in FB-IPv4.txt
5) Create 3 Firewall Rules to be allowed (TCP, UDP and UDPTCP)
  a) TCP Rules:
    i) Source: Internal Subnet
    ii) Destination: Whatspp_IPv4
    iii) Source Ports: Any
    iv) Destination Ports: Whatspp_TCP
  b) UDP Rules:
    i) Source: Internal Subnet
    ii) Destination: Whatspp_IPv4
    iii) Source Ports: Any
    iv) Destination Ports: Whatspp_UDP
  c) TCPUDP Rules:
    i) Source: Internal Subnet
    ii) Destination: Whatspp_IPv4
    iii) Source Ports: Any
    iv) Destination Ports: Whatspp_TCPUDP
