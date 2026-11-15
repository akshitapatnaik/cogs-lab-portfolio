# Lab 3.2 Findings – Server Monitoring Using Prometheus and Grafana

## Prometheus

- Open-source monitoring and alerting system.
- Collects server metrics using a pull-based model.
- Uses PromQL to query metrics.
- Collects CPU, memory, disk, and network metrics.
- Stores metrics as time-series data.

## Grafana

- Open-source visualization and dashboard platform.
- Connects to Prometheus as a data source.
- Displays server metrics using graphs and dashboards.
- Helps monitor CPU usage, memory usage, and network traffic.
- Supports alerts based on metric conditions.

## Node Exporter

- Collects hardware and operating system metrics from Linux servers.
- Provides CPU, memory, disk, and network metrics.
- Exposes metrics on port 9100.
- Allows Prometheus to scrape server metrics.

## Monitoring Panels Created

### 1. CPU Usage
- Monitors the percentage of CPU being used by the server.
- Helps identify high CPU utilization.
- Useful for checking server performance.

### 2. Memory Usage
- Monitors the RAM used by the server.
- Helps identify high memory consumption.
- Useful for preventing memory-related performance issues.

### 3. Network Traffic
- Monitors incoming and outgoing network traffic.
- Received traffic represents data coming into the server.
- Transmitted traffic represents data going out from the server.
- Uses network interface metrics such as `eth0`.

## Comparison

| Feature | Prometheus | Grafana | Node Exporter |
|---|---|---|---|
| Main Purpose | Monitoring | Visualization | Metric Collection |
| CPU Metrics | Collects | Displays | Exposes |
| Memory Metrics | Collects | Displays | Exposes |
| Network Metrics | Collects | Displays | Exposes |
| Query Language | PromQL | Uses data source queries | Not applicable |
| Dashboard | No built-in Grafana-style dashboard | Yes | No |
| Port | 9090 (default) | 3000 (default) | 9100 (default) |

## Conclusion

Prometheus, Grafana, and Node Exporter work together to monitor Linux server performance. Node Exporter collects system metrics, Prometheus scrapes and stores them, and Grafana visualizes the data through dashboards. This setup helps monitor CPU usage, memory consumption, and network traffic in real time and makes it easier to identify server performance issues.
