
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Azure Security Management and Compliance Framework</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.8;
            margin: 20px;
            background-color: #f7f7f7;
            color: #333;
        }

        h1,
        h2,
        h3 {
            color: #004080;
        }

        h1 {
            font-size: 2em;
            margin-bottom: 10px;
        }

        h2 {
            margin-top: 30px;
            font-size: 1.5em;
            border-bottom: 2px solid #004080;
            padding-bottom: 5px;
        }

        h3 {
            margin-top: 20px;
            font-size: 1.25em;
        }

        p {
            margin-bottom: 15px;
        }

        ul {
            list-style-type: square;
            margin-left: 20px;
        }

        code {
            background-color: #e8e8e8;
            padding: 2px 6px;
            border-radius: 4px;
        }

        .example-image {
            margin: 20px 0;
            text-align: center;
        }

        .example-image img {
            max-width: 100%;
            height: auto;
            border: 1px solid #ccc;
            border-radius: 8px;
        }

        .note {
            background-color: #eef5ff;
            padding: 10px;
            border-left: 5px solid #004080;
            margin-bottom: 20px;
        }
    </style>
</head>

<body>
    <h1>Azure Security Management and Compliance Framework</h1>

    <h2>Project Overview</h2>
    <p>This project involves creating a comprehensive security management and compliance framework within Azure. Advanced security controls were implemented, continuous monitoring for threats was set up, responses were automated, and compliance with industry standards was ensured—all key areas covered in the AZ-500 exam. This framework enhances security while streamlining operations and governance in a cloud environment.</p>

    <h2>1. Identity and Access Management (IAM)</h2>
    <h3>Objective:</h3>
    <p>Identities and access permissions in Azure were securely managed to protect sensitive information and prevent unauthorized access.</p>
    <h3>Tasks:</h3>
    <ul>
        <li><strong>Azure Active Directory (Azure AD):</strong>
            <ul>
                <li>Azure AD was set up and configured, integrating it with the existing on-premises Active Directory.</li>
                <li>Multi-factor authentication (MFA) was implemented for all users, requiring at least two verification methods for access.</li>
                <li>Conditional Access policies were configured to control access to resources based on conditions such as user location, device, or risk level.</li>
                <li>Self-Service Password Reset (SSPR) was enabled for users, reducing the burden on IT support while maintaining security.</li>
                <li>Azure AD Identity Protection was integrated to detect and respond to identity-based risks in real-time.</li>
            </ul>
        </li>
        <li><strong>Privileged Identity Management (PIM):</strong>
            <ul>
                <li>PIM was enabled to manage, control, and monitor access to important resources, providing just-in-time (JIT) access for critical roles.</li>
                <li>Approval workflows were implemented for role activations, ensuring that all elevated permissions were appropriately vetted.</li>
                <li>Privileged roles were audited and reviewed periodically to ensure compliance with least privilege principles.</li>
            </ul>
        </li>
        <li><strong>Role-Based Access Control (RBAC):</strong>
            <ul>
                <li>RBAC roles were assigned to grant the least privilege necessary for users, groups, and service principals, adhering to the principle of least privilege.</li>
                <li>Custom RBAC roles were created, tailored to specific job functions or project needs, ensuring that permissions were precisely aligned with requirements.</li>
                <li>Resource Tags and Management Groups were implemented to organize and secure Azure resources at scale, allowing for more granular access controls.</li>
            </ul>
        </li>
    </ul>

    <div class="example-image">
        <p><em>Example Image: A flowchart illustrating the implementation of Conditional Access policies with Azure AD, highlighting different decision points based on user risk levels.</em></p>
        <!-- Example Image would go here -->
    </div>

    <h2>2. Securing the Network Infrastructure</h2>
    <h3>Objective:</h3>
    <p>Network resources were protected using advanced security features and best practices to mitigate threats and ensure data confidentiality and integrity.</p>
    <h3>Tasks:</h3>
    <ul>
        <li><strong>Azure Firewall:</strong>
            <ul>
                <li>Azure Firewall was deployed and configured to control network traffic, filter based on policies, and log all traffic for audit purposes.</li>
                <li>Azure Firewall was integrated with Azure Monitor for advanced logging and analytics, enabling proactive threat detection.</li>
                <li>Threat intelligence-based filtering was implemented to block traffic from known malicious IP addresses automatically.</li>
            </ul>
        </li>
        <li><strong>Network Security Groups (NSGs):</strong>
            <ul>
                <li>NSGs were applied to secure virtual networks by filtering inbound and outbound traffic at both the subnet and NIC levels.</li>
                <li>Application Security Groups (ASGs) were used to group VMs by application or workload, simplifying NSG management.</li>
                <li>NSG rules were reviewed and updated regularly to ensure alignment with current security policies and practices.</li>
            </ul>
        </li>
        <li><strong>Azure DDoS Protection:</strong>
            <ul>
                <li>Azure DDoS Protection Standard was enabled to safeguard resources against distributed denial-of-service attacks, providing enhanced mitigation capabilities.</li>
                <li>DDoS Protection alerts were set up in Azure Monitor to notify security teams in the event of an attack.</li>
                <li>The effectiveness of DDoS protection was tested by simulating a controlled attack and reviewing the mitigation response.</li>
            </ul>
        </li>
    </ul>

    <div class="example-image">
        <p><em>Example Image: A network diagram showing Azure Firewall, NSGs, ASGs, and DDoS Protection in action, with data flow paths and security controls highlighted.</em></p>
        <!-- Example Image would go here -->
    </div>

    <h2>3. Managing and Monitoring Security Operations</h2>
    <h3>Objective:</h3>
    <p>Tools and processes for effective security operations, continuous monitoring, and rapid response to security incidents were implemented.</p>
    <h3>Tasks:</h3>
    <ul>
        <li><strong>Azure Security Center:</strong>
            <ul>
                <li>Azure Security Center was enabled to monitor the environment, provide security recommendations, and implement best practices across all Azure resources.</li>
                <li>Security Center was configured to integrate with existing security information and event management (SIEM) solutions, such as Azure Sentinel.</li>
                <li>Automated remediation was set up for common security issues identified by Security Center, reducing the time to respond to threats.</li>
            </ul>
        </li>
        <li><strong>Azure Sentinel (SIEM):</strong>
            <ul>
                <li>Azure Sentinel was set up to collect data, detect threats, and respond to incidents, leveraging built-in and custom analytics rules.</li>
                <li>Detection rules and alerts were created and configured to identify security incidents, using machine learning models to reduce false positives.</li>
                <li>Automated response playbooks were implemented in Sentinel to handle routine incidents, such as isolating compromised VMs or blocking malicious IPs.</li>
                <li>Azure Sentinel was integrated with external threat intelligence feeds to enhance the accuracy of threat detection and response.</li>
            </ul>
        </li>
        <li><strong>Log Analytics:</strong>
            <ul>
                <li>Log Analytics was used to aggregate and analyze data from various Azure services, enabling deep visibility into the environment.</li>
                <li>Custom queries and dashboards were created in Log Analytics to monitor key security metrics, such as failed login attempts or unusual network activity.</li>
                <li>Alerts were set up in Log Analytics for critical security events, ensuring timely notification of security teams.</li>
            </ul>
        </li>
    </ul>

    <div class="example-image">
        <p><em>Example Image: A screenshot of the Azure Sentinel dashboard showing active threats, alerts, and the integration of threat intelligence feeds.</em></p>
        <!-- Example Image would go here -->
    </div>

    <h2>4. Automating Security Responses</h2>
    <h3>Objective:</h3>
    <p>Automated solutions were developed to respond to security incidents quickly and efficiently, reducing human intervention and error.</p>
    <h3>Tasks:</h3>
    <ul>
        <li><strong>Azure Logic Apps:</strong>
            <ul>
                <li>Logic Apps were used to automate workflows between Azure services, triggering actions in response to security events detected by Azure Sentinel.</li>
                <li>Logic Apps were integrated with Azure Sentinel to trigger automated actions based on specific conditions, improving incident response times.</li>
                <li>Logic Apps were configured to interact with third-party services, enabling seamless workflows across multiple platforms.</li>
            </ul>
        </li>
        <li><strong>Azure Automation:</strong>
            <ul>
                <li>Azure Automation was used to deploy runbooks that performed routine tasks, such as patch management, VM shutdowns, and compliance checks.</li>
                <li>Automation tasks were scheduled to run during off-peak hours, minimizing the impact on production environments.</li>
                <li>The success of automation tasks was monitored, and parameters were adjusted as needed to ensure reliability and effectiveness.</li>
            </ul>
        </li>
        <li><strong>Custom Scripting:</strong>
            <ul>
                <li>Custom PowerShell scripts were developed to automate complex tasks, such as provisioning and configuring new resources with security best practices.</li>
                <li>Scripts were integrated with Azure Automation and Logic Apps for end-to-end automation, ensuring consistent and repeatable processes.</li>
                <li>Scripts were tested and validated in a controlled environment before deployment to production, ensuring they met security and operational requirements.</li>
            </ul>
        </li>
    </ul>

    <div class="example-image">
        <p><em>Example Image: A flowchart showing how Logic Apps, Azure Sentinel, and Automation work together to handle a security incident, from detection to resolution.</em></p>
        <!-- Example Image would go here -->
    </div>

    <h2>5. Compliance and Governance</h2>
    <h3>Objective:</h3>
    <p>Azure resources were ensured to comply with organizational policies and industry regulations through proper governance and auditing.</p>
    <h3>Tasks:</h3>
    <ul>
        <li><strong>Azure Policy:</strong>
            <ul>
                <li>Policies were defined and enforced using Azure Policy to ensure resources complied with organizational and regulatory standards.</li>
                <li>Initiatives in Azure Policy were implemented to apply a set of related policies across multiple resources for consistency.</li>
                <li>Azure Policy was configured to audit non-compliant resources and automatically remediate issues when possible.</li>
            </ul>
        </li>
        <li><strong>Azure Blueprints:</strong>
            <ul>
                <li>Azure Blueprints were used to define a repeatable set of resources that adhered to security and compliance requirements, streamlining the deployment process.</li>
                <li>Blueprints were assigned to new subscriptions to ensure that all resources deployed within those subscriptions met organizational standards.</li>
                <li>Blueprints were updated as policies or requirements changed, ensuring that all new deployments reflected the latest security practices.</li>
            </ul>
        </li>
        <li><strong>Compliance Manager:</strong>
            <ul>
                <li>Compliance Manager was used to assess the organization's compliance posture, identifying gaps and recommending actions to address them.</li>
                <li>Compliance scores were reviewed regularly, and relevant teams were worked with to close gaps and improve overall compliance.</li>
                <li>Compliance reports were generated for audits and management reviews, demonstrating adherence to industry regulations such as GDPR, HIPAA, or PCI DSS.</li>
            </ul>
        </li>
    </ul>

    <div class="example-image">
        <p><em>Example Image: A dashboard view of Azure Policy showing compliance status, policy definitions, and the number of resources affected by each policy.</em></p>
        <!-- Example Image would go here -->
    </div>
</body>

</html>
