# Detection Engineering Portfolio

**Building threat detection capabilities through hands-on lab work and practical implementation**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/tresean-tuggle-b36811138/)
[![Portfolio](https://img.shields.io/badge/Portfolio-View%20Projects-green)](#project-catalog)
[![Certifications](https://img.shields.io/badge/Certs-3%20Completed-orange)](#certifications--learning-path)

---

## About This Portfolio

This portfolio demonstrates end-to-end detection engineering capabilities developed over six months of intensive hands-on lab work (September 2025 - March 2026).

### The Journey

I transitioned into cybersecurity with a clear goal: become a Detection Engineer. Rather than passively consuming training content, I built a complete detection engineering workflow from the ground up, starting with endpoint telemetry collection, progressing through SIEM ingestion and alert development, and culminating in SOC-style investigations and MITRE ATT&CK-mapped detection logic.

**Timeline:**
- **September 2025:** Started from zero cybersecurity background
- **October-December 2025:** Earned CompTIA A+, ISC2 CC, and CompTIA Security+ certifications
- **Nov 2025 -March 2026:** Built 8+ detection engineering labs spanning multiple platforms and detection languages
- **Current:** Pursuing SC-200 (Microsoft Security Operations Analyst) certification

### What Makes This Portfolio Different

Most cybersecurity portfolios consist of isolated CTF writeups or certification study notes. This portfolio demonstrates a **coherent detection engineering workflow**:

1. **Endpoint Visibility** → Understanding what telemetry sources exist and how to collect them
2. **SIEM Ingestion** → Getting data into detection platforms at scale
3. **Detection Development** → Writing detection logic that identifies malicious behavior
4. **MITRE ATT&CK Mapping** → Translating threat intelligence into actionable detections
5. **SOC Operations** → Triaging alerts and distinguishing true positives from false positives
6. **Detection Tuning** → Improving signal-to-noise ratio through threshold adjustment and context-based validation

Each project builds on the previous one, demonstrating systematic skill progression rather than random lab exercises.

---

## Core Competencies

### Detection Engineering
- Develop detection logic across multiple query languages (Python, SPL, KQL, Sigma)
- Map detections to MITRE ATT&CK framework techniques and tactics
- Tune detection thresholds to optimize signal-to-noise ratio
- Build automated alert rules with configurable severity and response actions
- Correlate events across multiple data sources for high-fidelity detections

### SIEM Operations
- Ingest endpoint telemetry into cloud SIEM platforms (Splunk Cloud, Microsoft Sentinel)
- Configure data connectors and HTTP Event Collectors (HEC)
- Build security dashboards and workbooks for real-time monitoring
- Write complex queries for log analysis and threat hunting
- Create scheduled analytics rules with automated incident generation

### SOC & Incident Response
- Conduct SOC-style alert triage and investigation
- Perform false positive analysis and detection refinement
- Document investigation findings in structured incident reports
- Apply context-based validation (parent process, user context, host role)
- Communicate technical findings using standardized frameworks

### Endpoint Telemetry
- Deploy and configure Sysmon for enhanced process visibility
- Enable Windows Security auditing (Event ID 4688, command-line logging)
- Analyze process creation logs for suspicious execution patterns
- Correlate process execution with network activity (DNS, HTTP)
- Understand telemetry gaps and data source limitations

---

## Project Catalog

### 🔍 Endpoint Telemetry & Visibility

#### [Windows Endpoint Telemetry - Phase I](https://github.com/tdt1114/Windows-Endpoint-Telemetry-I)
**Foundation lab demonstrating endpoint logging configuration and SIEM ingestion**

- Installed and configured Sysmon for enhanced process visibility
- Enabled Windows Security Event ID 4688 with command-line logging
- Ingested process creation telemetry into Splunk Enterprise
- Documented real-world troubleshooting (service hangs, PID locks, Event Viewer issues)

**Skills:** Sysmon deployment, Windows auditing, Splunk ingestion, PowerShell verification

---

#### [Windows Endpoint Telemetry - Phase II: SOC Triage](https://github.com/tdt1114/Windows-Endpoint-Telemetry-II-SOC-Triage)
**Extended telemetry lab with cloud SIEM and SOC-style investigation**

- Ingested Sysmon and Event ID 4688 logs into Splunk Cloud via HTTP Event Collector (HEC)
- Conducted SOC-style alert triage and investigation
- Performed false positive analysis and documented findings
- Built SPL queries for detection and analysis

**Skills:** Splunk Cloud, HEC configuration, SOC operations, alert investigation, SPL query development

---

#### [Process-Network Correlation Lab](https://github.com/tdt1114/process-network-correlation-lab)
**Multi-source event correlation for behavioral detection**

- Correlated Windows process execution with DNS and network activity
- Analyzed temporal relationships between Sysmon Event ID 1 and DNS Client logs
- Demonstrated how single events produce low confidence but correlation improves signal quality
- Mapped correlated behavior to MITRE ATT&CK techniques (T1059.001, T1071.001, T1071.004)

**Skills:** Event correlation, behavioral analysis, multi-source detection, investigative reasoning

---

### 🎯 MITRE ATT&CK & Detection Logic

#### [MITRE ATT&CK Mapping Lab](https://github.com/tdt1114/MITRE-mapping)
**Analyst-focused lab demonstrating threat-informed detection**

- Analyzed encoded PowerShell execution and mapped to T1059.001
- Created Sigma detection rule for platform-agnostic detection logic
- Documented analyst reasoning for why technique mapping applies
- Demonstrated context-based validation (parent process, user context, host role)

**Skills:** MITRE ATT&CK framework, Sigma rule writing, detection reasoning, encoded PowerShell analysis

---

### 🛡️ SIEM Platforms & Detection Development

#### [Azure AD Sign-In Analyzer](https://github.com/tdt1114/azure-ad-signin-analyzer)
**Foundation project for cloud identity threat detection**

- Analyzed Azure AD sign-in logs for authentication anomalies
- Built detection logic for brute force and credential stuffing attacks
- Extended into Python and KQL detection labs (see sub-projects below)

**Skills:** Azure AD log analysis, authentication monitoring, cloud identity security

---

#### [Python Detection Lab](https://github.com/tdt1114/azure-ad-signin-analyzer/tree/main/python-detection-lab)
**Automated detection pipeline using Python**

- Built 4-script detection workflow: simulate → parse → detect → report
- Simulated brute force attacks against Azure AD accounts
- Implemented configurable alert thresholds for false positive reduction
- Generated automated incident reports with recommended actions

**Skills:** Python scripting, detection automation, threshold tuning, incident reporting

---

#### [KQL & Microsoft Sentinel Lab](https://github.com/tdt1114/azure-ad-signin-analyzer/tree/main/kql-sentinel-lab)
**Cloud-native SIEM with automated detection rules**

- Deployed Microsoft Sentinel and connected Entra ID Audit Logs
- Wrote KQL queries for identity change detection and privilege escalation
- Built automated analytics rule mapped to MITRE ATT&CK Privilege Escalation tactic
- Created security workbook with real-time dashboards for alerts and incidents
- Simulated privilege escalation by assigning Global Reader role

**Skills:** Microsoft Sentinel, KQL query language, automated alert rules, MITRE ATT&CK mapping, workbook creation

---

### 📊 Additional Projects

#### [Hybrid Active Directory Lab](https://github.com/tdt1114/hybrid-active-directory-lab)
**Enterprise identity infrastructure deployment and administration**

- Deployed hybrid Active Directory environment in Microsoft Azure
- Configured domain controller (Windows Server 2022) and domain workstation (Windows 10 Enterprise)
- Performed identity administration: user provisioning via PowerShell, security group assignment, delegated administration
- Implemented Group Policy for password policies and logon scripts
- Validated authentication, authorization, and role-based access control
- Foundation for future identity-based threat detection scenarios

**Skills:** Active Directory, Azure infrastructure, identity management, Group Policy, PowerShell automation, delegated administration

---

#### DMARC Email Security Analysis
**Email authentication protocol analysis for phishing prevention**

*Repository link coming soon*

---
## Technical Skills

### SIEM & Security Platforms
- **Splunk:** Splunk Cloud, Splunk Enterprise, HTTP Event Collector (HEC), SPL query language
- **Microsoft Sentinel:** Workspace deployment, data connectors, analytics rules, workbooks, KQL
- **Azure/Entra ID:** Audit logs, sign-in logs, identity monitoring

### Detection & Query Languages
- **Python:** Log parsing, anomaly detection, automated reporting, threshold-based alerting
- **SPL (Splunk Processing Language):** Search queries, statistical analysis, correlation searches
- **KQL (Kusto Query Language):** Detection queries, summarization, time-series analysis
- **Sigma:** Platform-agnostic detection rule format, YAML-based rule writing

### Endpoint Telemetry & Logging
- **Sysmon:** Installation, configuration, Event ID 1 (process creation), Event ID 3 (network connections)
- **Windows Security Logs:** Event ID 4688 (process creation), command-line auditing, auditpol configuration
- **DNS Client Logs:** DNS query analysis, process-network correlation
- **Event Viewer:** Log analysis, custom views, PowerShell log queries

### Frameworks & Methodologies
- **MITRE ATT&CK:** Technique mapping (T1059.001, T1071.001, T1071.004, Privilege Escalation tactics)
- **Detection Engineering:** Threat-informed detection, behavioral analytics, multi-source correlation
- **SOC Operations:** Alert triage, incident investigation, false positive analysis, detection tuning

### Cloud & Infrastructure
- **Microsoft Azure:** Virtual networks, resource groups, VM deployment, hybrid environments
- **Active Directory:** Domain controllers, organizational units, Group Policy, delegated administration
- **PowerShell:** Automation, log analysis, system administration

### Development & Tools
- **Version Control:** Git, GitHub, commit workflows, repository documentation
- **Scripting:** Python 3.x, PowerShell, Bash
- **Troubleshooting:** Service debugging, log correlation, root cause analysis

---
## Certifications & Learning Path

### Completed Certifications

| Certification | Date | Focus Area |
|--------------|------|------------|
| **CompTIA A+** | October-November 2025 | Hardware, networking, operating systems, security fundamentals |
| **ISC2 Certified in Cybersecurity (CC)** | December 2025 | Security principles, governance, risk management |
| **CompTIA Security+** | December 2025 | Threats, attacks, vulnerabilities, security architecture |

### In Progress

**SC-200: Microsoft Security Operations Analyst**  
*Target completion: Q2 2026*

Focus areas:
- Mitigate threats using Microsoft Sentinel
- Mitigate threats using Microsoft Defender
- Query, visualize, and monitor data in Microsoft Sentinel
- Configure and manage automation in Microsoft Sentinel

### Additional Training

- **TryHackMe Advent of Cyber** (December 2025 - January 2026)
- Ongoing security research and tool evaluation

### Timeline: Zero to Detection Engineer in 6 Months
```
September 2025    → Started from zero cybersecurity background
October 2025      → CompTIA A+ Core 1
November 11, 2025     → CompTIA A+ Core 2
December 5, 2024  → ISC2 CC
December 19, 2024 → CompTIA Security+
November 2025 -March 2026 → Built 8 detection engineering labs
March 2026        → Current: Pursuing SC-200, applying for Detection Engineer roles
```

**What This Demonstrates:**  
Exceptional learning velocity, self-direction, and the ability to rapidly acquire new technical skills—critical traits for detection engineering roles where threats and technologies evolve constantly.

---
## Contact & Connect

I'm actively seeking Detection Engineer, Security Engineer, or SOC Analyst roles where I can apply and expand these skills in a production environment.

### Let's Connect

- **LinkedIn:** [linkedin.com/in/tresean-tuggle-b36811138](https://www.linkedin.com/in/tresean-tuggle-b36811138/)
- **GitHub:** [@tdt1114](https://github.com/tdt1114)
- **Email:** tresean.tuggle@gmail.com

### What I'm Looking For

I'm seeking opportunities to:
- Build and tune detections in production environments
- Work with experienced detection engineers and threat intelligence teams
- Gain hands-on experience with enterprise-scale SIEM deployments
- Contribute to SOC operations and incident response workflows
- Continue learning emerging detection techniques and threat actor TTPs

**Open to:** Full-time Detection Engineer, Security Engineer, or SOC Analyst II roles  
**Location:** Remote or hybrid opportunities  
**Current Status:** Actively interviewing

---

## Repository Structure
```
detection-engineering-portfolio/
├── README.md                    # This file - portfolio overview
└── certifications/
    ├── README.md               # Certification overview and study resources
    ├── comptia-a-plus.md       # CompTIA A+ study guide
    ├── isc2-cc.md              # ISC2 CC study guide
    ├── security-plus.md        # CompTIA Security+ study guide
    └── sc-200.md               # SC-200 study guide (in progress)
```

---

## Acknowledgments

This portfolio represents 6 months of intensive self-directed learning. Special thanks to the cybersecurity community for open-source tools, documentation, and guidance that made this possible.

**Built with:** Splunk, Microsoft Sentinel, Azure, Python, Sysmon, MITRE ATT&CK  
**Inspired by:** Real-world SOC operations and detection engineering workflows  
**Purpose:** Demonstrate practical detection engineering capabilities to future employers

---

*Last updated: March 2026*
