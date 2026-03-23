# CloudGate

## Objective

CloudGate is a cloud-native Zero Trust security platform designed to secure employee access, monitor authentication behavior, and detect unauthorized access attempts. The project focuses on implementing identity-based access control, centralized logging, and automated alerting in a cloud environment to simulate real-world security monitoring and incident detection.

### Skills Learned

- Implementation of Zero Trust security principles.
- Identity and Access Management (IAM) configuration and role-based access control
- Secure application deployment using containerization (Docker)
- Log analysis and security event monitoring in cloud environments
- Detection of unauthorized access attempts (HTTP 403/401 patterns)
- Cloud-based incident investigation and forensic analysis
- Alert creation and monitoring for suspicious activity
- Understanding of cloud-native security architecture (Google Cloud)

### Tools Used
#### Cloud Platforms & Security
- Google Cloud Platform (GCP)
- Cloud IAM
- Identity-Aware Proxy (IAP)
- Cloud Logging & Logs Explorer
- Cloud Monitoring & Alert Policies
#### Deployment
- Docker & Dockerfile
- Google Cloud SDK (gcloud)
- Cloud Run
- Artifact Registry
#### Development
- Python
- Flask
- HTML

## Steps
#### Problem Identification & Architecture Design
- Lack of identity control
- No centralized logging
- No monitoring system
- <img width="628" height="472" alt="image" src="https://github.com/user-attachments/assets/cce69774-2145-4325-b8e1-b36aa63d7b83" />
#### Application Development
Built two main components:
 - Public Portal (open access landing page)
 - Employee Portal (dashboard with logging)
 - <img width="628" height="472" alt="image" src="https://github.com/user-attachments/assets/5ce44cdf-7cc3-4585-9f49-86abfdf6b5f6" />
 
#### Containerization & Deployment
- Packaged applications using Docker
- Pushed images to Artifact Registry
- Deployed services using Cloud Run:
- Public service
- Secure employee service
- <img width="600" height="307" alt="image" src="https://github.com/user-attachments/assets/963bb553-fd43-489a-b15c-d4538bb9c5f6" />

#### Zero Trust Security Implementation
##### Enforced authentication using:
- Google Identity login
- IAM roles (Cloud Run Invoker)
- Identity-Aware Proxy (IAP)
##### Implemented access control:
- Authorized users → HTTP 200
- Unauthorized users → HTTP 403
<img width="1918" height="1016" alt="image" src="https://github.com/user-attachments/assets/0d6770c7-d0ba-4193-8db4-f2fa7dee7a6c" />


#### Logging & Security Monitoring
- Enabled centralized logging using Cloud Logging
  ##### Analyzed:
- Successful access logs
- Failed authentication attempts
- Access patterns and timestamps

#### Attack Simulation & Detection
##### Simulated attack scenario:
- Multiple denied access attempts (incognito sessions)
- One successful authorized login
##### Observed:
- Unauthorized requests blocked at IAM layer
- - <img width="713" height="254" alt="image" src="https://github.com/user-attachments/assets/7a9f93a2-fd62-41f3-bad4-3d42ef0f01c2" />

#### Alerting & Automation
##### Configured alert policies for:
- Multiple failed login attempts
- Unusual access behavior
##### Integrated notification channels (email alerts)

#### Evidence Storage & Forensics
- Created secure cloud storage bucket
##### Stored:
- Logs
- Screenshots
- Incident reports
- Timeline documentation
- <img width="573" height="307" alt="image" src="https://github.com/user-attachments/assets/95902e18-d8ed-47a7-a31a-341172df5b00" />

### Future Enhancements
- Evidence integrity verification using SHA-256 hashing
- Integration of Web Application Firewall (WAF) for attack prevention


