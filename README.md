# Meridian Health Network: Incident Response Assessment

This project assesses a simulated cybersecurity incident at Meridian Health Network and develops recommendations for establishing a structured incident response program. It covers incident severity classification, RACI role assignments, initial incident communications, HIPAA breach notification considerations, and the six-phase incident response lifecycle.

## Table of Contents

- [Project Overview](#project-overview)
- [Network Topology](#network-topology)
- [Tools and Technologies](#tools-and-technologies)
- [Configuration Steps](#configuration-steps)
- [Results and Findings](#results-and-findings)
- [Author](#author)

## Project Overview

Meridian Health Network operates 12 clinics and a data center, with cloud-hosted patient records, a patient portal, telehealth services, third-party billing integrations, and clinician VPN access.

The scenario describes three security indicators:

- **Potential ransomware activity:** Encrypted file shares at two clinics.
- **Phishing attempt:** An email impersonating IT Support.
- **Suspicious account activity:** Unusual after-hours logins from a former contractor account.

The organization lacks a formal incident response plan, clearly defined response responsibilities, and tested playbooks.

The objectives of this project were to:

- Identify potential incidents and assign appropriate severity levels.
- Develop a RACI matrix for five incident response roles.
- Define internal communication priorities for the first 30 to 60 minutes.
- Assess potential HIPAA breach notification obligations.
- Apply the six-phase incident response lifecycle.
- Recommend improvements to incident response governance and operational readiness.

## Network Topology

The scenario describes a hybrid healthcare environment consisting of cloud-hosted services, on-premises infrastructure, clinic systems, and external service providers.

```text
                 Meridian Health Network
                           |
          +----------------+----------------+
          |                |                |
      12 Clinics        Data Center     Cloud Services
          |                |             (Azure)
          |                |                |
       EHR Access     On-Prem AD       Patient Records
          |                |                |
          +----------------+----------------+
                           |
                  Network and VPN Access
                           |
             +-------------+-------------+
             |                           |
       Clinician VPN              External Vendors
                                         |
                               Billing and Claims
```

The diagram represents a simplified logical view of the environment described in the scenario. Exact IP addresses, subnet configurations, firewall rules, and detailed network connections were not provided.

## Tools and Technologies

- **Incident Response Lifecycle:** Preparation, Detection and Analysis, Containment, Eradication, Recovery, and Post-Incident Activity.
- **RACI Matrix:** Defines Responsible, Accountable, Consulted, and Informed roles.
- **Microsoft Azure:** Cloud platform identified in the scenario.
- **Active Directory:** On-premises identity infrastructure identified in the scenario.
- **Clinician VPN:** Remote access technology used by clinicians.
- **Electronic Health Records (EHR):** Systems supporting clinical records and patient care.
- **HIPAA:** Regulatory framework relevant to protected health information and breach notification.
- **ISO/IEC 27001:** Referenced as a security management standard for the incident response program context.
- **PDF:** Documents the completed incident response assessment.
- **GitHub:** Hosts the project and supporting documentation.

No specific SIEM platform, endpoint detection tool, forensic utility, or firewall product was identified in the source scenario.

## Configuration Steps

1. **Assess the incident indicators.** Reviewed the encrypted file shares, phishing email, suspicious contractor account activity, and lack of incident response readiness.

2. **Assign severity levels.** Classified the encrypted file shares as potentially critical, the phishing email as requiring investigation, and the former contractor login as a high-priority security concern.

3. **Define incident response responsibilities.** Developed a RACI matrix for the Incident Commander, IT/Network Lead, Legal and Compliance, Communications Lead, and Business/Clinical Leadership.

4. **Establish initial communication priorities.** Identified the stakeholders who should be notified within the first 30 to 60 minutes and recommended a centralized incident communication channel.

5. **Recommend containment measures.** Proposed isolating affected systems where appropriate, disabling suspicious accounts, revoking active sessions, and preserving relevant evidence.

6. **Assess potential HIPAA obligations.** Identified the need for Legal and Privacy personnel to investigate possible exposure of protected health information and determine whether notification requirements apply.

7. **Apply the incident response lifecycle.** Mapped preparation, detection and analysis, containment, eradication, recovery, and post-incident activities to the scenario.

8. **Recommend program improvements.** Proposed a formal incident response plan, threat-specific playbooks, tabletop exercises, recovery testing, and remediation tracking.

9. **Document the assessment.** Prepared a report containing the findings, responsibilities, response priorities, and recommended improvements.

## Results and Findings

The assessment identified several weaknesses that could delay an effective incident response.

### Key Findings

- **Potential ransomware activity:** Encryption affecting two clinics could disrupt clinical operations and requires immediate investigation.
- **Phishing risk:** The email impersonating IT Support requires investigation to determine whether credentials were exposed or malware executed.
- **Access control weakness:** The former contractor account may remain active or may have been compromised, requiring prompt investigation and access revocation.
- **Incident response readiness:** The absence of a formal plan and reliance on one responder create accountability, coordination, and response-capacity risks.
- **Communication and compliance:** Technical response, clinical continuity, and privacy assessment must be coordinated from the beginning.

### Recommended Improvements

- Establish a formal incident response policy and documented escalation criteria.
- Assign an Incident Commander and define response responsibilities.
- Develop playbooks for ransomware, phishing, compromised accounts, third-party incidents, and potential PHI exposure.
- Test backup restoration, account deprovisioning, monitoring, and network isolation procedures.
- Conduct tabletop exercises involving IT, Legal, Privacy, Communications, and Clinical Operations.
- Document decisions, preserve evidence, track corrective actions, and review lessons learned.

**Compliance consideration:** The scenario raises potential HIPAA breach concerns, but the available information does not establish that a reportable breach occurred. The organization must assess the facts, determine whether unsecured PHI was involved, and apply the relevant breach notification requirements.

The project demonstrates how a GRC or incident response analyst can assess security events, coordinate stakeholders, document responsibilities, and recommend improvements to organizational preparedness.

## Author

- **Project:** Meridian Health Network Incident Response Assessment
- **Specialization:** Governance, Risk, and Compliance (GRC)
- **Focus Areas:** Incident Response, Severity Classification, RACI, Security Incident Communications, HIPAA, and Incident Response Governance
