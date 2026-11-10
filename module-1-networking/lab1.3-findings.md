# **Lab 1.3 Findings – WireGuard VPN to ZTNA Component Mapping**

## **1. WireGuard Components and ZTNA Equivalents**

| **WireGuard Component** | **ZTNA Equivalent** |
|---|---|
| VM2 (Client) | ZTNA Agent |
| VM1 (Server) | ZTNA Gateway |
| Public/Private Keys | Cryptographic Identity / Device Credentials |
| WireGuard Tunnel | Encrypted Secure Tunnel |
| Handshake | Authentication |
| AllowedIPs | Access Policy |
| UDP Port 51820 | Secure Communication Channel |
| Peer Configuration | Agent and Gateway Configuration |
| Key Management | Identity and Credential Management |

## **2. Verification and Testing**

- Configured WireGuard on both Ubuntu VMs (VM1 – Server and VM2 – Client).
- Started the WireGuard server and client services successfully.
- Verified the WireGuard interface using `sudo wg show` on both VMs.
- Confirmed a successful handshake between the client and server.
- Tested VPN connectivity using `ping -c 5 10.0.0.1` from VM2.
- Successfully received 5 out of 5 packets with **0% packet loss**.
- Used `sudo tcpdump -i ens5 -n udp port 51820` to capture WireGuard UDP traffic.
- Captured **24 packets** with **0 packets dropped**, confirming encrypted tunnel traffic.

## **3. Conclusion**

This lab demonstrates the basic concepts of Zero Trust Network Access (ZTNA) using WireGuard VPN. The client (VM2) establishes a secure connection with the server (VM1) using cryptographic keys. The handshake verifies the peer, while the encrypted tunnel protects communication. AllowedIPs controls which IP traffic is routed through the VPN.

WireGuard does not have a separate Controller like InstaSafe ZTNA. However, its peer configuration and key management demonstrate related identity and access-management concepts.

