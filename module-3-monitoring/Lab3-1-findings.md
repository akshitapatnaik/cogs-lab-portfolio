# lab3-1-findings

## Monitor Type Mapping

| **Uptime Kuma Monitor** | **Purpose** | **InstaSafe / Enterprise Use** |
| ----------------------- | ----------- | ------------------------------ |
| HTTP(S) | Checks website availability and HTTP response status | Gateway and portal health monitoring |
| TCP Port | Checks whether a specific service port is open and accepting connections | SSH, HTTPS, and service port availability |
| Ping | Checks whether a server is reachable over the network | Network connectivity and server reachability monitoring |

## Gateway Monitoring Rationale

Monitoring the InstaSafe Gateway is important because it acts as the main entry point for users to access applications and services. If the gateway becomes unavailable, users may not be able to access these services. HTTP(S), TCP Port, and Ping monitors help identify service failures, port connectivity issues, and network problems quickly. This helps the IT team respond to incidents and restore services faster.

## Lab 3.1 Conclusion

Successfully deployed Uptime Kuma and configured three monitors for the target VM. Stopped Nginx to test failure detection and observed a DOWN alert. Restarted Nginx and confirmed that the HTTP(S) monitor returned to UP with a 200 OK response.
