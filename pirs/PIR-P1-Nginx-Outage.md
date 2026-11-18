# Post-Incident Report (PIR)

## Incident Summary

- Reviewed the P1 Nginx Gateway Unreachable incident.
- Understood the impact of the Nginx outage on web application availability.
- Reviewed the incident response and recovery process.

## Timeline

- Reviewed the Uptime Kuma outage alert.
- Studied the GitHub issue creation and customer acknowledgement.
- Checked the investigation steps using Uptime Kuma logs and Prometheus metrics.
- Reviewed the investigation updates and resolution communication.
- Documented the Nginx restart and service recovery.

## Root Cause

Identified that the Nginx service was stopped, which caused the web application to become unavailable.

## Resolution

Reviewed the recovery command:

`sudo systemctl start nginx`

Verified that Uptime Kuma showed the service as healthy after restarting Nginx.

## Customer Impact

- Understood that users could not access the web application during the outage.
- Reviewed the impact on service availability.

## Lessons Learned

- Learned how monitoring tools help detect service outages.
- Understood the P1 incident response process.
- Practiced incident tracking and communication using GitHub Issues.
- Learned the importance of documenting service recovery.

## Preventive Actions

- Recommended enabling automatic restart for Nginx.
- Reviewed continuous monitoring through Uptime Kuma and Prometheus.
