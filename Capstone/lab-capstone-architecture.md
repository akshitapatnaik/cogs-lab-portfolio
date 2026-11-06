# Lab Capstone – Mini ZTNA Implementation

## Objective

To set up a basic Zero Trust Network Access (ZTNA) system using WireGuard, Nginx, Keycloak, and Uptime Kuma.

---

## Architecture Diagram

```text
              User Laptop
           (WireGuard Client)
                10.0.0.2
                    |
             Secure VPN Tunnel
                    |
                    ▼
             VM2 (10.0.0.1)
        ┌──────────────────────┐
        │  WireGuard Server    │
        │  Nginx Reverse Proxy │
        └──────────┬───────────┘
                   |
              HTTP Proxy
                 (/app)
                   |
                   ▼
             VM1 (Keycloak)
                Port 8080

               Uptime Kuma
          (Service Monitoring)
```

---

## Components

- **Laptop:** Connects to the VPN using WireGuard.
- **VM2:** Provides VPN access and handles requests through Nginx.
- **VM1:** Hosts Keycloak for identity management and authentication.
- **Uptime Kuma:** Checks whether the services are available.

---

## Request Flow

```text
Laptop
   ↓
WireGuard VPN
   ↓
VM2 – Nginx Proxy
   ↓
VM1 – Keycloak
```

---

## Verification

Run the following commands to check the services:

```bash
sudo wg
sudo nginx -t
curl http://10.0.0.1/app
```

The curl command is used to check whether the Keycloak application can be reached through the VPN tunnel and Nginx proxy.

---

## Results

- WireGuard VPN connection established.
- Nginx reverse proxy configuration tested.
- Keycloak application accessed through the `/app` path.
- Uptime Kuma set up to monitor services.
- Communication between the laptop, gateway, and application server tested.

---

## Evidence

- WireGuard VPN connection screenshot.
- Output of the `sudo wg` command.
- Nginx configuration test screenshot.
- Output of the curl request.
- Uptime Kuma monitoring dashboard screenshot.
- `docker ps` output showing the Keycloak container.
