# Lab 5.1 – Findings

## Objective

To simulate a P1 incident, investigate the service outage, restore Nginx, and complete the incident response process.

## My Work

I intentionally stopped the Nginx service on my AWS Ubuntu server to simulate a P1 incident.

I used Uptime Kuma to detect and monitor the service outage. I created a P1 GitHub issue to track the incident and document the investigation.

I restarted Nginx using:

sudo systemctl start nginx

I verified that the service was running successfully and Uptime Kuma showed the recovery status as healthy.

## Key Learnings

- Learned how to identify and respond to P1 incidents.
- Practiced monitoring service availability using Uptime Kuma.
- Learned how to create and manage incident tickets using GitHub Issues.
- Understood service recovery, incident documentation, PIR, and PACE processes.
