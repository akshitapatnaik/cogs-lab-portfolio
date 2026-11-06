
# Lab Capstone – Mini ZTNA Architecture

## Objective

Build a mini Zero Trust Network Access (ZTNA) environment using WireGuard, Nginx, Keycloak, and Uptime Kuma.

## Environment

- Cloud Platform: Oracle Cloud Infrastructure (OCI)
- Operating System: Ubuntu 22.04
- VM1: Application Server
- VM2: Gateway Server
- Laptop: WireGuard Client

## Architecture Diagram

```text
             Laptop
        (WireGuard Client)
             10.0.0.2
                 |
                 |
          WireGuard VPN Tunnel
                 |
                 v
            VM2 (10.0.0.1)
        ---------------------
        | WireGuard Server   |
        | Nginx Reverse Proxy|
        ---------------------
                 |
                 |
            HTTP Proxy
              (/app)
                 |
                 v
          VM1 (Application Server)
                 |
              Keycloak
            (Port 8080)

             Uptime Kuma
             (Monitoring)
```

## Components

1. **Laptop** – Runs the WireGuard Client.
2. **VM2 – Gateway Server** – Runs WireGuard Server and Nginx Reverse Proxy.
3. **VM1 – Application Server** – Runs Keycloak Identity Provider.
4. **Uptime Kuma** – Monitors service availability.
5. **Prometheus** – Collects system and application metrics.

## Request Flow

1. The user connects the laptop to the VM2 Gateway Server using WireGuard.
2. WireGuard establishes an encrypted VPN tunnel.
3. The user sends a request to the Nginx Reverse Proxy on VM2.
4. Nginx forwards the request to the Keycloak application running on VM1.
5. Keycloak handles the identity and authentication process.
6. Uptime Kuma monitors service availability.
7. Prometheus collects monitoring metrics.

## Verification

The following commands will be used after configuration:

```bash
sudo wg
sudo nginx -t
curl http://10.0.0.1/app
```

## Results

To be updated after successful implementation and testing.

## Evidence

- Screenshot of WireGuard connection.
- Screenshot of `sudo wg`.
- Screenshot of `sudo nginx -t`.
- Screenshot of application access using curl.
- Screenshot of Keycloak dashboard.
- Screenshot of Uptime Kuma dashboard.

## Conclusion

This project demonstrates a simplified Zero Trust Network Access architecture using a secure VPN tunnel, reverse proxy, identity provider, and monitoring system.
