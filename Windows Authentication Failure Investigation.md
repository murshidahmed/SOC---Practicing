# Windows Authentication Failure Investigation

ATTEMPT: 01

What I investigated:
  -  Few failed login alerts (Rule ID 60122)

Decision:
  - Classified a false positive

Reason:
  - User generated failed login attempts
  - No malicious indicators


ATTEMPT: 02

What I investigated:
  -  Many failed login alerts (Rule ID 60122)

Decision:
  - Suspicious behaviour, but still false positive

Reason:
  - Local machine
  - Same user
  - You were physically present
  - No external IP
  - No account lockout

