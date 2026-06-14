# AI-Enhanced Network Architecture
### WGU — ODN1 Task 1 (E026) | Pruhart Health Network Modernization

---

## Overview

This project presents a scalable, AI-enhanced network architecture designed for Pruhart Health — a regional healthcare provider that recently acquired two independent clinics and specialty care centers. The goal was to unify fragmented legacy infrastructure into a secure, intelligent, and future-ready network capable of supporting telehealth, electronic health records (EHR), and AI-assisted diagnostics.

The design covers three major areas: architecture and scalability, AI-driven security, and network automation and optimization.

---

## Repository Contents

| File | Description |
|---|---|
| `README.md` | Project overview and documentation |
| `network-diagram.pdf` | AI-assisted network architecture diagram (Lucidchart export) |
| `pruhart-health.gns3project` | GNS3 portable project file |
| `screenshots/` | Supporting screenshots of tools used |

---

## Part 1 — Network Architecture Design

### Core Network Components

**HQ Router (192.168.1.1/24)**
Central gateway between internal VLANs and external connections. Manages inter-VLAN routing and DMZ traffic. Included to serve as the primary traffic controller across all network segments.

**DMZ Router (192.168.3.1/24)**
Isolates public-facing services from internal systems. Reduces the attack surface by ensuring external traffic never reaches internal resources directly.

**Core Switch (192.168.2.2/24)**
Backbone of the LAN. Interconnects VLANs and ensures efficient data flow between servers, staff devices, and IoT systems.

**Access Switches (Switch 1, Switch 2)**
Connect end-user devices to the network. Enforce VLAN segmentation policies for staff and IoT traffic.

**EHR Server (192.168.20.10)**
Hosts electronic health records. Requires high availability, encryption, and strict access control given the sensitivity of patient data.

**File Server (192.168.20.20)**
Centralized storage for documents and shared resources. Supports clinical and administrative operations across all locations.

**Backup Server (192.168.20.30)**
Provides data redundancy and disaster recovery. Critical for HIPAA compliance and operational continuity.

**Wireless Access Points — WAPs (192.168.30.2/28, 192.168.1.2/28)**
Extend network access to wireless devices across staff and IoT VLANs. Support mobility and flexible device deployment.

**Azure Cloud Shell**
Enables remote management, automation, and monitoring. Provides elastic compute capacity for cloud bursting and offloading.

**AI Processing Units**
Embedded within the server VLAN and cloud infrastructure. Support real-time analytics, anomaly detection, and automated decision-making.

---

### Scalability

**Horizontal Scaling**
- Modular VLAN design allows new devices and services to be added without disrupting existing infrastructure
- Azure Cloud Shell enables rapid deployment of virtual machines and containers
- Additional switches can be deployed to support physical expansion across acquired clinic locations

**Vertical Scaling**
- Servers in VLAN 20 (EHR, File, Backup) can be upgraded with additional CPU, memory, or storage
- AI tools monitor usage trends and predict when vertical scaling is needed before performance degrades
- Cloud compute bursting shifts workloads temporarily when local resources are at capacity

**Resource Management Techniques**
- AI-assisted load balancing dynamically routes requests to least-congested servers
- Predictive scaling provisions resources ahead of demand spikes such as peak patient hours
- Dynamic bandwidth allocation prioritizes critical services like EHR access and telemedicine
- Anomaly detection triggers automated responses including rerouting and provisioning

---

### KPI Comparison — AI-Enhanced vs. Existing Architecture

| KPI | Existing Network | AI-Enhanced Network |
|---|---|---|
| Latency | High and variable — static routing | Lower and stable — AI dynamically reroutes traffic |
| Throughput | Limited by fixed configurations | Higher via AI load balancing and cloud elasticity |
| Fault Tolerance | Reactive — manual intervention required | Proactive — predictive analytics and automated failover |

Estimated improvements: latency reduced 20 to 40%, throughput increased through dynamic load balancing, fault tolerance significantly improved through predictive maintenance.

---

## Part 2 — AI-Enhanced Network Security

### IDS/IPS Solution

The design incorporates **Azure Sentinel** with AI-driven threat detection, positioned between the HQ Router and DMZ Router and monitoring traffic within the Server VLAN. It uses machine-learning analytics to detect anomalies, malicious behavior, and unauthorized access attempts across both on-premises and cloud-connected segments.

**Why Azure Sentinel:**
- Learns normal traffic patterns and identifies zero-day threats through behavioral analysis
- Scales across VLANs and cloud services without manual reconfiguration
- Protects high-value assets including EHR, File, and Backup servers
- Automates responses such as blocking IPs, isolating devices, and rerouting traffic

### Malware Detection Approaches

- Signature-based detection for known threats using updated global signatures
- Heuristic and behavioral analysis for unusual file access or privilege escalation
- AI-enhanced sandboxing executing suspicious files in isolation
- Anomaly detection flagging deviations from baseline network behavior
- Predictive modeling anticipating emerging malware based on trend data

### Automated Incident Response Mechanisms

**Mechanism 1 — AI-Driven Device Isolation**
When suspicious behavior is detected such as abnormal traffic or unauthorized access, AI automatically quarantines the affected device, blocking communication with critical VLANs and preventing lateral movement.

**Mechanism 2 — Automated Threat Remediation**
AI applies corrective actions including blocking malicious IPs, updating firewall and IDS/IPS rules, resetting compromised credentials, and initiating malware removal — reducing time between detection and containment.

---

## Part 3 — AI Tools for Network Automation and Optimization

### Tool Evaluation

The selected AI tool continuously analyzes traffic patterns, device performance, and configuration states to automate routine tasks and improve efficiency.

**Performance Improvements**
Reduces manual configuration time, improves routing efficiency, and minimizes downtime by predicting congestion and automatically adjusting network paths.

**Compared to Traditional Management**
Traditional network management relies on manual monitoring and static configurations, which are slower and more prone to error. AI-based management uses real-time analytics and automated decision-making to adapt instantly to changing conditions.

**Evaluation Framework**
Effectiveness is tracked using key metrics including latency, throughput, error rates, and automated task success rates. Regular audits compare AI-generated actions to expected outcomes to ensure accuracy and alignment with organizational policies.

### Cost and Benefit Analysis

| | Details |
|---|---|
| Cost 1 | Licensing and subscription fees for AI-driven platforms |
| Cost 2 | Additional infrastructure and compute resources for AI processing |
| Benefit 1 | Reduced operational workload — automation frees IT staff for higher-value work |
| Benefit 2 | Improved network performance and reliability — less downtime, faster issue detection |

### Resource Utilization

AI algorithms and automation scripts require additional memory and CPU cycles for log analysis, telemetry processing, and predictive modeling. Bandwidth consumption increases slightly due to continuous data collection. These overheads are small relative to the performance gains achieved.

**Optimization Strategy**
- Run AI analytics during off-peak hours
- Use cloud-based compute bursting for heavy workloads
- Apply tiered resource allocation prioritizing critical systems
- Regularly tune AI models and automation scripts to eliminate unnecessary consumption

---

## Tools Used

- **Lucidchart** — AI-assisted network architecture diagram
- **GNS3** — Network simulation and portable project export
- **Azure Sentinel** — AI-powered IDS/IPS and threat detection
- **Azure Cloud Shell** — Remote management and cloud automation
- **GitLab** — Version control and project hosting

---

## References

Microsoft. (2024). *What is Microsoft Sentinel?* https://learn.microsoft.com/en-us/azure/sentinel/overview

Cisco. (2024). *Cisco Secure IPS.* https://www.cisco.com/c/en/us/products/security/ngips/index.html

GNS3. (2024). *GNS3 documentation.* https://docs.gns3.com

Lucidchart. (2024). *Network diagram software.* https://www.lucidchart.com
