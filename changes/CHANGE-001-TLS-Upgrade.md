\# CHANGE-001: TLS Upgrade



\## Change Details



\- \*\*Change ID:\*\* CHANGE-001

\- \*\*Type:\*\* Normal Change

\- \*\*Status:\*\* Pending Approval

\- \*\*Description:\*\* Update Nginx TLS configuration to prefer TLS 1.3.

\- \*\*Justification:\*\* TLS 1.3 provides improved security and performance and follows current security best practices.

\- \*\*Environment:\*\* AWS Ubuntu Lab Server



\## Objective



Enable TLS 1.3 on the Nginx web server and disable TLS 1.2.



\## Implementation Plan



1\. Back up the existing Nginx TLS configuration.

2\. Update the `ssl\_protocols` directive to TLS 1.3 only.

3\. Test the configuration using `sudo nginx -t`.

4\. Reload the Nginx service.

5\. Verify TLS 1.3 using OpenSSL.

6\. Verify that TLS 1.2 connections are rejected.



\## Risk Assessment



\- Incorrect configuration may make the website unavailable.

\- Older TLS clients may not be able to connect.

\- Nginx configuration errors may prevent service reload.



\## Rollback Trigger



Rollback will be initiated if:

\- Nginx configuration testing fails.

\- TLS 1.3 verification fails.

\- The website becomes unreachable.



\## Rollback Plan



1\. Restore the backed-up `lab-tls` configuration.

2\. Run `sudo nginx -t`.

3\. Reload Nginx.

4\. Verify website availability using `curl -k https://localhost`.



\*\*Rollback Time Target:\*\* Under 2 minutes.



\## Maintenance Window



Immediate — isolated lab environment with no production customer impact.



\## Verification Plan



\- Nginx configuration test successful.

\- TLS 1.3 handshake successful.

\- TLS 1.2 handshake rejected.

\- Website accessible after the change.



\## Approval



\*\*Change Status:\*\* Pending Approval



The change will only be executed after this plan has been committed to GitHub.



\## Execution Outcome



Pending.



\## Rollback Outcome



Pending.

