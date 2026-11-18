# Post-Incident Report (PIR) – My Part

## Incident Summary

I reviewed the MFA OTP delivery incident that affected 25 users at a financial institution. The issue occurred because Kaleyra rejected SMS messages due to a flagged sender ID.

## Timeline

- Reviewed the customer complaint and P2 ticket creation.
- Checked the investigation timeline and Kaleyra rejection status.
- Understood the escalation process from L1 to L2 support.
- Reviewed the activation of the backup sender ID at 11:40 IST.
- Recorded customer confirmation of service restoration at 11:45 IST.

## Root Cause

Identified the flagged SMS sender ID as the main reason for OTP delivery failure.

## Impact Assessment

- Reviewed the impact on 25 users.
- Understood how MFA failure affected user authentication and business operations.
- Noted the increased support workload.

## Resolution Steps

1. Reviewed the incident details and customer report.
2. Studied the Kaleyra API rejection status.
3. Understood the escalation to L2 support.
4. Reviewed the backup sender ID activation.
5. Documented successful OTP delivery.
6. Recorded customer confirmation of service restoration.

## Prevention Actions

- Documented the need to monitor SMS gateway rejection rates.
- Reviewed the recommendation for automatic backup sender ID failover.

## Key Learnings

- Learned how to analyze MFA-related incidents.
- Understood the L1-to-L2 escalation process.
- Learned the importance of incident timelines and root cause analysis.
- Understood how PIR documentation helps prevent recurring incidents.
