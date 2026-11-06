# PACE Handover – Nginx Gateway Incident

## Incident Details

- **Incident ID:** INC-001
- **Priority:** P1 – Critical
- **Issue:** Nginx Gateway Unavailable
- **Status:** In Progress

---

## Primary

Check whether the Nginx service is running properly.

```bash
sudo systemctl status nginx
```

Verify that the Uptime Kuma monitor shows the correct service status.

---

## Alternate

If Nginx is stopped, try restarting the service.

```bash
sudo systemctl restart nginx
```

Check whether the website responds:

```bash
curl http://localhost
```

---

## Contingency

If the problem continues:

- Check the Nginx error logs.
- Review CPU and memory usage in Prometheus.
- Check firewall rules and network connectivity.
- Review the Nginx configuration.

---

## Emergency

If the gateway remains unavailable:

- Escalate the issue to the Infrastructure Team.
- Restore the last working configuration if required.
- Inform the concerned team about the service interruption.
- Provide status updates every 15 minutes until recovery.

---

## Handover Notes

- Keep monitoring Nginx availability.
- Record all troubleshooting activities.
- Update the incident status after verification.
- Document the final resolution.
