# Azure Security Management and Compliance Framework

## Project Overview
This project involves creating a comprehensive security management and compliance framework within Azure. Advanced security controls were implemented, continuous monitoring for threats was set up, responses were automated, and compliance with industry standards was ensured. This framework enhances security while streamlining operations and governance in a cloud environment.

## 1. Identity and Access Management (IAM)

### Objective
Identities and access permissions in Azure were securely managed to protect sensitive information and prevent unauthorized access.

### Tasks

- **Azure Active Directory (Entra AD):**
  - Entra was set up and configured.
  - Multi-factor authentication (MFA) was implemented for all users, requiring at least two verification methods for access.
  - Conditional Access policies were configured to control access to resources based on conditions such as user location, device, or risk level.
  - Self-Service Password Reset (SSPR) was enabled for users, reducing the burden on IT support while maintaining security.
  - Azure AD Identity Protection was integrated to detect and respond to identity-based risks in real-time.

- **Privileged Identity Management (PIM):**
  - PIM was enabled to manage, control, and monitor access to important resources, providing just-in-time (JIT) access for critical roles.
  - Approval workflows were implemented for role activations, ensuring that all elevated permissions were appropriately vetted.
  - Privileged roles were audited and reviewed periodically to ensure compliance with least privilege principles.

- **Role-Based Access Control (RBAC):**
  - RBAC roles were assigned to grant the least privilege necessary for users, groups, and service principals, adhering to the principle of least privilege.
  - Custom RBAC roles were created, tailored to specific job functions or project needs, ensuring that permissions were precisely aligned with requirements.
  - Resource Tags and Management Groups were implemented to organize and secure Azure resources at scale, allowing for more granular access controls.

<img src="https://i.imgur.com/8Lrxk4U.png"/>

## 2. Securing the Network Infrastructure

### Objective
Network resources were protected using advanced security features and best practices to mitigate threats and ensure data confidentiality and integrity.

### Tasks

- **Azure Firewall:**
  - Azure Firewall was deployed and configured to control network traffic, filter based on policies, and log all traffic for audit purposes.
  - Azure Firewall was integrated with Azure Monitor for advanced logging and analytics, enabling proactive threat detection.
  - Threat intelligence-based filtering was implemented to block traffic from known malicious IP addresses automatically.

- **Network Security Groups (NSGs):**
  - NSGs were applied to secure virtual networks by filtering inbound and outbound traffic at both the subnet and NIC levels.
  - Application Security Groups (ASGs) were used to group VMs by application or workload, simplifying NSG management.
  - NSG rules were reviewed and updated regularly to ensure alignment with current security policies and practices.

- **Azure DDoS Protection:**
  - Azure DDoS Protection Standard was enabled to safeguard resources against distributed denial-of-service attacks, providing enhanced mitigation capabilities.
  - DDoS Protection alerts were set up in Azure Monitor to notify security teams in the event of an attack.
  - The effectiveness of DDoS protection was tested by simulating a controlled attack and reviewing the mitigation response.

<img src="https://i.imgur.com/TnZBvKR.png"/>

## 3. Managing and Monitoring Security Operations

### Objective
Tools and processes for effective security operations, continuous monitoring, and rapid response to security incidents were implemented.

### Tasks

- **Microsoft Defender for Cloud:**
  - Microsoft Defender for Cloud was enabled to monitor the environment, provide security recommendations, and implement best practices across all Azure resources.
  - Microsoft Defender for Cloud was configured to integrate with existing security information and event management (SIEM) solutions, such as Azure Sentinel.
  - Automated remediation was set up for common security issues identified by Security Center, reducing the time to respond to threats.

- **Microsoft Sentinel (SIEM):**
  - Microsoft Sentinel was set up to collect data, detect threats, and respond to incidents, leveraging built-in and custom analytics rules.
  - Detection rules and alerts were created and configured to identify security incidents, using machine learning models to reduce false positives.
  - Automated response playbooks were implemented in Sentinel to handle routine incidents, such as isolating compromised VMs or blocking malicious IPs.
  - Microsoft Sentinel was integrated with external threat intelligence feeds to enhance the accuracy of threat detection and response.

- **Log Analytics:**
  - Log Analytics was used to aggregate and analyze data from various Azure services, enabling deep visibility into the environment.
  - Custom queries and dashboards were created in Log Analytics to monitor key security metrics, such as failed login attempts or unusual network activity.
  - Alerts were set up in Log Analytics for critical security events, ensuring timely notification of security teams.

<img src="https://i.imgur.com/gY73an5.png"/>

## 4. Automating Security Responses

### Objective
Automated solutions were developed to respond to security incidents quickly and efficiently, reducing human intervention and error.

### Tasks

- **Azure Logic Apps:**
  - Logic Apps were used to automate workflows between Azure services, triggering actions in response to security events detected by Azure Sentinel.
  - Logic Apps were integrated with Azure Sentinel to trigger automated actions based on specific conditions, improving incident response times.
  - Logic Apps were configured to interact with third-party services, enabling seamless workflows across multiple platforms.
<img src="https://i.imgur.com/49xQ2ZG.png"/>

- **Azure Automation:**
  - Azure Automation was used to deploy runbooks that performed routine tasks, such as patch management, VM shutdowns, and compliance checks.
  - Automation tasks were scheduled to run during off-peak hours, minimizing the impact on production environments.
  - The success of automation tasks was monitored, and parameters were adjusted as needed to ensure reliability and effectiveness.

- **Custom Scripting:**
  - Custom PowerShell scripts were developed to automate complex tasks, such as provisioning and configuring new resources with security best practices.
  - Scripts were integrated with Azure Automation and Logic Apps for end-to-end automation, ensuring consistent and repeatable processes.
  - Scripts were tested and validated in a controlled environment before deployment to production, ensuring they met security and operational requirements.

<img src="https://i.imgur.com/UqdG0rt.png"/>

## 5. Compliance and Governance

### Objective
Azure resources were ensured to comply with organizational policies and industry regulations through proper governance and auditing.

### Tasks

- **Azure Policy:**
  - Policies were defined and enforced using Azure Policy to ensure resources complied with organizational and regulatory standards.
  - Initiatives in Azure Policy were implemented to apply a set of related policies across multiple resources for consistency.
  - Azure Policy was configured to audit non-compliant resources and automatically remediate issues when possible.

- **Azure Blueprints:**
  - Azure Blueprints were used to define a repeatable set of resources that adhered to security and compliance requirements, streamlining the deployment process.
  - Blueprints were assigned to new subscriptions to ensure that all resources deployed within those subscriptions met organizational standards.
  - Blueprints were updated as policies or requirements changed, ensuring that all new deployments reflected the latest security practices.

- **Microsoft Purview Compliance Manager:**
  - Compliance Manager was used to assess the organization's compliance posture, identifying gaps and recommending actions to address them.
  - Compliance scores were reviewed regularly, and relevant teams were worked with to close gaps and improve overall compliance.
  - Compliance reports were generated for audits and management reviews, demonstrating adherence to industry regulations such as GDPR, HIPAA, or PCI DSS.

<img src="https://i.imgur.com/Chyd9N4.png"/>

