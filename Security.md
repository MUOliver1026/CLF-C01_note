# Security and Compliance

- **25%** of the exam
- Define the AWS shared responsibility model
- Define the AWS Cloud security and compliance concepts
- Identify AWS access management capabilities
- Identify resources for receiving security-related support

## Security in the Cloud

### IT Infrastructure: Present-Day AWS Cloud

- Global network of data centers built with security in mind
- Safeguards to protect customer privacy
- Dozens of compliance programs to help meet industry compliance requirements for data security

### Shared Responsibility Model

Security of cloud computing infrastructures and data is a `shared responsibility` between the customer and AWS

- Security **of** the Cloud (**AWS**)
- Security **in** the Cloud (**You/Customer**)

#### AWS: Security of the Cloud

- AWS is responsible for protecting the infrastructure:
  - Physical security of `data centers` hosting the AWS Cloud
  - Security of hardware, software, networking, and so on, that runs the cloud computing services (`physical server`)

#### You: Security in the Cloud

- You are responsible for varying levels of security functions, depending on the AWS Cloud service used, such as:
  - Protecting customer data and data encryption
  - Identity and Access Management
  - Patching operating systems of VMs
  - Configuring firewalls

### Security in a Well-Architected IT Infrastructure

Secure from **external and internal threats**

#### Recall: Five pillars of the Well-Architected Framework

1. Operational Excellence
2. `Security`
3. Reliability
4. Performance Efficiency
5. Cost Optimization

#### Security pillar

- **Identity and Access Management (IAM)**
  - Actively manage all-user access
  - Use strong identity foundation
  - `Principle of least privilege`
- **Detective Controls**
  - Enable traceability: "Who did what, when?"
  - Actively monitor alerts
  - Audit actions and changes to environment in real time
- **Infrastructure Protection**
  - Apply security `on all layers` of infrastructure
  - Not just the outer layer like the physical data center
  - Virtual servers: secure multiple layers like subnet, load balancer, and OS
  - Security best practices should be automated to save time and money when scaling
- **Data Protection**
  - Security mechanisms should be adjusted depending on sensitivity of the data
  - Keep people away from data
- **Incident Response**
  - Intervene, investigate, and deal with all security events
  - Once issue is resolved, update incident management process
  - Continue to learn from past mistakes and security events

### Principle of least privilege

- Only provide access to resources an entity requires to do its job

- Permission should be no more or no less than the optimal level of access

- Use Identity Access Management (IAM) in the AWS Cloud

- Coincides with the shared responsibility model

## Security Services

### Identity and Access Management (IAM)

- Manage access to services and resources on the AWS Cloud
- Manage users and groups
- Can provide access to users or other AWS services
- Permissions are global: any access setting will be true across all regions
- Follow principle of least privilege

#### Ways to set permissions

1. **Manage Users**
   - Create users in IAM and assign them security credentials
   - Users can have very precise permission sets
   - User can access AWS through AWS Management Console
   - You can provide programmatic access to data/resources
   - Programmatic access: applications directly accessing resources instead of humans doing the same activity
2. **Manage IAM Roles**
   - Create roles to manage permissions and what those roles can do
   - An entity assumes a role to obtain temporary security credentials to make API calls to your resources
   - Used to provide access to a user from another AWS account to your AWS account
3. **Manage Federated Users**
   - Enable identity federation: allow existing identites in your enterprise to access AWS without having to create IAM user for each identityIdeal for lists
   - Can use any identity management solution using SAML 2.0 or one of AWS's federation samples

#### Benefits

- Enhanced security
- Granular control
- Ability to provide temporary credentials
- Flexible security credential management
- Federated access
- Seamless integration across various AWS services

### Web application firewall (WAF)

- Protects web apps running on the AWS Cloud from common web exploits
- Firewall service for web applications
- Protect web apps against exploits that could compromise security or availability
- Protect apps from exploits that could force your app to consume excessive resources

- Improves web traffic visibility 
- Provides cost-effective web app protection
- Increased security and protection against web attacks
- Easy to deploy and maintain

### AWS Shield

#### Distributed Denial of Service (DDoS) Attack

- An attempt to make a machine or network resource unavailable
- Most often by making excessive repeated requests to the website using thousands of unique IP adresses

#### AWS Shield

- Provides detection and automatic mitigations
- Minimise effects of DDoS attacks to your apps
- Helps minimise application downtime and latency when an attack happens

#### AWS Shield: Standard

- Automatically enabled
- Free
- Protects web applications against a majority of common DDoS attacks
- Get comprehensive availablitiy protection against all known infrastructure attacks when used with CouldFront and Route 53

#### AWS Shield: Advanced

- Continuous, 24/7 access to AWS DDoS response team
- Near real-time visibility into events
- Integrates with AWS WAF
- Provides higher-level protections, network and transport layer protections, and automated application traffic monitoring
- Finanical protection againstt DDoS-related spikes in charges for EC2, elastic load balancers, CloudFront, and Route 53
- Available globally on all CloudFront and Route 53 Edge locations
- Your web application can be hosted anywhere in the world and still be protected by AWS Shield

### Amazon Inspector

- Automated secuity assessment service for applications
- Automatically asssess for exposure, vulnerabilities, and dervations from best practices
- Generates detailed reports to help check for vulnerabilities
- Security teams can get reports validating that tests were performed
- Reduce risk of introducing security issues during deployment and development
- You can define standards and best practices
- Or use the AWS constantly updated standards

### AWS Trusted Advisor

- Guides provisioning of resources to follow AWS best practices
- Scans your infrastructure and advises you on how it is or is not folling AWS best practices
- Based on five categories: cost optimization, performance, security, fault tolerance, service limits
- Provides action recommendations to meet best practices

#### Seven Core Trusted Advisor Checks

1. S3 bucket permissions
2. Security groups - specific ports unrestricted
3. IAM use
4. MFA on root account
5. EBS public snapshots
6. RDS public snapshots
7. Service limits

#### Full Trusted Advisor Checks

- More types of checks on top of core checks
- Notifications through weekly updates
- Set up automated actions in response to alerts using CloudWatch
- Programmatic access to scan results via AWS Support API

### GuardDuty

- 24/7 threat detection service for the AWS Cloud 
- Monitors for malicious activity and unauthorized behaviour
- Analyzes events to send actionable alerts via CloudWatch
- Uses machine learning, anomaly detection, and integrated threat intelligence to identify potential threats
- Easy to deploy