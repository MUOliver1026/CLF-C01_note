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