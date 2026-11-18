# Lab 5.2 – Findings

## Objective

To perform a safe TLS configuration change on the Nginx server, test the change, and practice the rollback procedure.

## My Work

- Created and committed the CHANGE-001 TLS upgrade plan to GitHub before making any changes.
- Backed up the existing Nginx configuration.
- Updated the TLS configuration to allow TLS 1.3 only.
- Tested the configuration using `sudo nginx -t`.
- Reloaded Nginx and verified TLS 1.3 using OpenSSL.
- Confirmed that TLS 1.2 connections were rejected.
- Simulated a configuration failure using an invalid `ssl_protocolz` directive.
- Restored the backup configuration and verified that Nginx was working again.
- Checked service availability using `curl -k -I https://localhost`.

## Key Learnings

- Learned the importance of change planning and approval before implementation.
- Practiced secure TLS configuration.
- Understood how to test configuration changes before reloading services.
- Learned how to perform rollback during a failed change.
- Understood the importance of maintaining a Git commit history for change tracking.
