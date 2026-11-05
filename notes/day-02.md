# Day 2: IP addressing and subnets

## Concepts
- IP address: the address of a device on a network, like 192.168.1.25 (four numbers, 0 to 255).
- Private IPs are used inside a network (10.x, 172.16-31.x, 192.168.x). Public IPs are reachable on the internet.
- Subnet: a smaller group of addresses inside a bigger network.
- CIDR (the slash number): how many bits are the network part. Addresses = 2^(32 - slash). A /24 has 256 addresses.
- DNS: turns names like google.com into IP addresses.

## My laptop
- IPv4: 10.0.0.45 (private)
- Subnet mask: 255.255.255.0 (/24)
- Default gateway: 10.0.0.1 (my router)
- ping 8.8.8.8: 0% loss, about 18 ms
- nslookup google.com: answered by the Rogers DNS server, returned public IPs (192.178.x.x)

## Azure lab
- Created vnet-day02 (10.0.0.0/16) in rg-day02.
- Subnets: web 10.0.1.0/24 and db 10.0.2.0/24.
- Each subnet showed 251 available IPs (256 minus 5 reserved by Azure).
- Deleted rg-day02 afterwards so nothing keeps running.

## Quick check
1. Public vs private: private is only used inside a network, public is reachable on the internet.
2. A /24 holds 256 addresses (254 usable on a normal network).
3. DNS translates names into IP addresses.
