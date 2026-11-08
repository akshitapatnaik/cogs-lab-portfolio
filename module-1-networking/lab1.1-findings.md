# Lab 1.1 Findings

## My VM Details

- Provider: AWS
- Region: ap-southeast-2 (Sydney)
- OS: Ubuntu
- Private IP: 172.31.26.158

## Experiment Results

### Ping to 8.8.8.8

- Average RTT: 1.180 ms
- TTL value observed: 119
- What does TTL tell us about the path? - TTL indicates how many router hops a packet can travel before it expires. It helps us understand the approximate network distance to the destination.

### Traceroute to google.com

- Number of hops: 4
- Any `* * *` hops? Yes
- At which hop number? Hop 1 (one probe) in the normal traceroute; hop 2 (all probes) in the TCP traceroute.

### DNS Comparison

- **Result from default DNS:**
- DNS Server: 127.0.0.53
- Resolved IPv4 Address: 142.251.222.238
- Resolved IPv6 Address: 2404:6800:4006:804::200e

- **Result from 1.1.1.1:**
- DNS Server: 1.1.1.1
- Resolved IPv4 Address: 142.251.222.238
- Resolved IPv6 Address: 2404:6800:4006:807::200e

- Are they different? Yes, the IPv6 addresses are different, but the IPv4 address is the same. Different DNS servers may return different addresses due to caching, load balancing, and geographic routing.

### Nmap Port Scan

- Command: `nmap -sV localhost`
- Open Port: 22/tcp
- Service: SSH
- Version: OpenSSH 10.2p1 Ubuntu
- Closed TCP ports: 999

### TCP Connection to google.com

- Command: `curl -v https://www.google.com 2>&1 | head -40`
- HTTPS Port: 443
- TLS Version: TLS 1.3
- HTTP Protocol: HTTP/2
- Connection: Successful using IPv4
- IPv6 connection: Network unreachable

### google.com TLS Certificate

- Issuer: Google Trust Services (CN = WE2)
- Subject: CN = *.google.com
- Expiry date: Dec 30, 2026
- TLS version used: TLS 1.3

## Conclusion

All six networking experiments were completed successfully on my AWS EC2 Ubuntu server. I learned how to use ping, traceroute, nslookup, dig, nmap, curl, and OpenSSL to understand network connectivity, DNS resolution, open ports, HTTPS connections, and SSL certificates.
