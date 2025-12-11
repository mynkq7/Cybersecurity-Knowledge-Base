## Incident Response

### Incidents

Any unauthorized event, planned or accidental, that negatively impacts digital assets.

Examples:

- Denial of service
- Data leaks
- Security breaches
- Malware infections

* * *

### Incident Response Framework

#### 1. Preparation

Building necessary resources to handle the incident.

**Resources include:**

- Developing incident response teams
- Having proper incident response plans in place
- Deploying necessary security solutions

* * *

#### 2. Identification

Looking for abnormal behaviors that may indicate an incident.

**Involves:**

- Using various security solutions and techniques
- Monitoring abnormal events

**Common Tools:**

- **SIEM:** Collects logs in a centralized location and correlates them to identify incidents.
- **AV:** Detects known malicious programs and scans regularly.
- **EDR:** Protects endpoints, contains and eradicates advanced threats.

* * *

#### 3. Containment

Minimizing the impact of the attack.  
Usually done by:

- Isolating the victim machine
- Disabling compromised user accounts

* * *

#### 4. Eradication

- Removing the threat from the affected environment
- Ensuring the environment is clean

* * *

#### 5. Recovery

- Recovering affected systems from backups or rebuilding them
- Testing and validating recovered systems before reuse

* * *

#### 6. Lessons Learned

- Document gaps in detection and analysis
- Improve processes for future incidents

* * *

### Playbooks vs Runbooks

| Term | Description |
| --- | --- |
| **Playbook** | Step-by-step instructions to deal with incidents. |
| **Runbook** | Step-by-step execution of specific steps during different incidents. |

* * *

### Incident Response Teams (CIRT)

- Called on demand
- Handle critical incidents
- Perform deep forensic analysis
- Recover breached systems
- Identify hidden threats
- Support SOC with analysis

**Incident Response Team Roles:**

- Forensic Lead
- CSIRT Manager
- Threat Intelligence Expert
- Threat Hunting Expert
- Malware Analyst

* * *

### Specialized Defensive Roles

#### Digital Forensic Analyst

- Uncovers hidden threats in memory and disk.

#### Threat Intelligence Analyst

- Gathers data about emerging threat groups.

#### Application Security Engineer

- Maintains a secure software development lifecycle.

#### AI Researcher

- Studies AI threats and develops defensive strategies.

* * *

### 3. Technology

Security solutions minimize the SOC team’s manual effort to detect and respond to threats.

**Common Tools:**

- SIEM
- EDR
- Firewalls