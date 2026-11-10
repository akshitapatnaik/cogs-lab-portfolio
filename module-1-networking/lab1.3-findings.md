# Lab 1.3 Findings – WireGuard VPN to ZTNA Component Mapping

## 1. WireGuard Components and ZTNA Equivalents

| WireGuard Component | ZTNA Equivalent |
|---|---|
| VM2 (Client) | ZTNA Agent |
| VM1 (Server) | ZTNA Gateway |
| Public/Private Keys | Device Identity |
| WireGuard Tunnel | Encrypted Secure Tunnel |
| Handshake | Authentication |
| AllowedIPs | Access Policy |
| Encrypted UDP (51820) | Secure Communication |

## 2. Verification

- Configured WireGuard on both Ubuntu VMs.
- Verified the WireGuard interface using `wg show`.
- Checked the handshake between the client and server.
- Tested connectivity by pinging `10.0.0.1` from VM2.
- Used `tcpdump` to capture UDP traffic on port 51820 and verify encrypted tunnel traffic.

## 3. Conclusion

WireGuard demonstrates the core concept of Zero Trust Network Access (ZTNA). The client (agent) establishes a secure connection with the gateway using cryptographic keys. The tunnel encrypts communication, while AllowedIPs controls which traffic can pass through the connection.

Similar to a ZTNA solution, communication is authenticated, encrypted, and restricted to authorized endpoints.
