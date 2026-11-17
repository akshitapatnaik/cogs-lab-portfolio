# My Contribution – Post-Incident Report (PIR)

## Ticket #1 – MFA SMS OTP Failure

**Severity:** P2 – High  
**Product:** MFA  
**Environment:** Production  
**Affected Users:** 25 Finance department users

### My Work

- Created and documented the P2 incident ticket in GitHub.
- Investigated the SMS OTP delivery issue using the Kaleyra dashboard findings.
- Identified bulk REJECTED status codes for all 25 affected numbers.
- Added an internal investigation note documenting possible DND registration or sender ID blocking.
- Escalated the issue to L2 with the impact, findings and required actions.
- Documented the root cause, resolution and prevention steps in the resolution summary.

### Resolution and Outcome

- A backup sender ID was used in the lab scenario.
- OTP delivery was verified using test numbers.
- Customer confirmation was documented.
- All 25 affected users were reported to have received SMS OTPs successfully.

### Prevention Recommendations

- Enable sender ID monitoring.
- Maintain a backup sender ID.
- Monitor SMS delivery failures proactively.

### Learning

I learned how to document a P2 incident, add internal notes, escalate an issue to L2, track ticket status and prepare a resolution summary using GitHub Issues.
