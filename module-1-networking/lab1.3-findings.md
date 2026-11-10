Lab 1.3 Findings – WireGuard VPN to ZTNA Component Mapping

1. WireGuard Components and ZTNA Equivalents
WireGuard Component	ZTNA Equivalent
VM2 (Client)	ZTNA Agent
VM1 (Server)	ZTNA Gateway
Public/Private Keys	Cryptographic Identity / Device Credentials
WireGuard Tunnel	Encrypted Secure Tunnel
Handshake	Authentication
AllowedIPs	Access Policy
UDP Port 51820	Secure Communication Channel
Peer Configuration	Gateway and Agent Configuration
Key Management	Identity and Credential Management

2. Verification
- Configured WireGuard on both Ubuntu VMs.
- Started the WireGuard server on VM1 and client on VM2.
- Verified the VPN interface using sudo wg show on both VMs.
- Confirmed a successful handshake between client and server.
- Tested connectivity using ping -c 5 10.0.0.1 from VM2.
- Received 5 out of 5 packets with 0% packet loss.
- Used sudo tcpdump -i ens5 -n udp port 51820 to capture encrypted UDP traffic.
- Captured 24 packets with 0 packets dropped.
  
3. Conclusion
WireGuard demonstrates the basic concepts of Zero Trust Network Access (ZTNA). The client establishes a secure connection with the gateway using cryptographic keys. The handshake verifies the peer, and the encrypted tunnel protects communication. AllowedIPs controls which IP traffic is routed through the VPN.

WireGuard does not have a separate Controller like InstaSafe ZTNA. However, its peer configuration and key management demonstrate some related identity and access-management concepts.
4. Key Learning
- Understood how a VPN tunnel works between two cloud VMs.
- Learned how cryptographic keys authenticate WireGuard peers.
- Practiced Linux networking commands and traffic monitoring.
- Understood the relationship between VPN technology and ZTNA architectur
