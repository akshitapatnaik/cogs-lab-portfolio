# CHANGE-001 – Nginx Server Configuration Update

**Change ID:** CHANGE-001

**Type:** Normal Change

**Description:** Update the Nginx server configuration to improve web server security and reliability.

**Justification:** Proper Nginx configuration helps protect the web server and ensures reliable website access.

## Execution Steps

1. Backup the current Nginx configuration.
2. Review the existing server configuration.
3. Update the required security settings.
4. Test the configuration using `nginx -t`.
5. Reload the Nginx service.
6. Verify that the website is accessible.

## Rollback Trigger

If the Nginx configuration test fails or the website becomes unreachable.

## Rollback Steps

1. Restore the previous Nginx configuration.
2. Test the restored configuration.
3. Reload the Nginx service.
4. Verify that the website is working.

**Rollback Commands:**

```bash
sudo cp /etc/nginx/nginx.conf.backup /etc/nginx/nginx.conf
sudo nginx -t
sudo systemctl reload nginx
```

**Rollback Time:** 2 minutes (estimated)

**Maintenance Window:** Immediate (Lab Environment)
