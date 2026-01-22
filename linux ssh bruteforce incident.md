
# SSH Brute-Force Attack Detection and Response

## 1. Summary
A series of unauthorized SSH login attempts were detected on a Linux server using Wazuh SIEM. The activity was identified as a brute-force attack and successfully mitigated using Fail2Ban.

## 2. Environment
- SIEM: Wazuh (Open-source)
- Server OS: Ubuntu Server
- Endpoint OS: Windows 11
- Attacker Simulation: Kali Linux
- Network: Isolated NAT Network

## 3. Detection
Multiple Wazuh alerts were triggered related to SSH authentication failures, including attempts to log in using non-existent users and repeated password failures.

## 4. Investigation
The alerts originated from a remote system and occurred within a short time window. The repeated nature of the attempts and use of invalid usernames indicated malicious behavior rather than user error.

## 5. Incident Classification
This activity was classified as a **real security incident** (SSH brute-force attack).

## 6. Response and Mitigation
Fail2Ban was installed and configured on the Ubuntu server to automatically block IPs after repeated failed login attempts. SSH was further hardened by limiting authentication retries.

## 7. Verification
After mitigation, the attacker IP was successfully banned by Fail2Ban, and further SSH attempts were blocked.

## 8. Conclusion
The incident demonstrated effective detection, analysis, and response using a SIEM-based approach. This lab simulates a real-world SOC incident lifecycle.
