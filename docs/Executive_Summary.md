# Executive Summary: Hospitality Business Security Audit

## Business Context
Modern hospitality operations rely heavily on integrated Point-of-Sale (POS) systems, digital payment gateways, and guest Wi-Fi amenities. Due to high staff turnover and fast-paced multi-shift environments, cybersecurity controls in Horeca venues are frequently compromised by convenience.

This assessment evaluated the operational security posture of a local hospitality venue to identify critical vulnerabilities affecting financial transactions and network continuity.

## Key Vulnerabilities & Business Impact

1. **Guest & Transaction Network Convergence**
   * **Finding:** Public guest devices share the same network infrastructure as POS payment endpoints and management machines.
   * **Impact:** An attacker on guest Wi-Fi could perform network reconnaissance, intercept unencrypted traffic, or exploit vulnerable POS components.

2. **Shared Credentials & Lack of Accountability**
   * **Finding:** Administrative and POS terminal override accounts are shared across multiple staff shifts using static/default credentials.
   * **Impact:** Inability to audit unauthorized voids, discounts, or configuration changes to specific employees.

3. **Database Backup Resilience**
   * **Finding:** Transaction and inventory databases are backed up locally on primary drives without offsite or immutable storage.
   * **Impact:** Complete data loss or operational disruption in the event of hardware failure or ransomware infection.

## Priority Action Plan
* **Immediate (Week 1):** Isolate Guest Wi-Fi via dedicated VLAN; enforce individual staff PINs/logins on POS terminals.
* **Short-Term (Month 1):** Deploy automated offsite cloud backups for sales data and secure physical network equipment in a locked rack.
