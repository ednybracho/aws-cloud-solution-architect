# Security and the AWS Shared Responsability Model

## Who ultimately is responsable for security in AWS?

- a) You (customer)
- b) AWS?
- c) Correct Response: Both you and AWS are responsable for securiting your AWS Envorinment.

## Shared Responsability Model:

- This distinction of responsability is commonly referred to as Security OF the cloud, versus Security IN the cloud.
- It's important to consider which AWS service you use and review the level of responsibility required to sercure the service.

### Customer

- Responsability for security 'in' the cloud
  - Customer Data
  - Platform, Applications, Identity and Access Management
  - Operating Systems, Network, and Firewall Configuration (Patching & Upgrades)
    - Customer-side Data Encryption and Data Integrity Authentication
    - Server-side Encryption (File System and/or Data)
    - Networking Traffic Protection (Encryption, Integrity, Identity)

### AWS

- Responsability for security 'of' the cloud
  - Software (Trhough Virtualization)
    - Compute
    - Storage
    - Database
    - Networking
  - Hardware or AWS Global Infrastructure
    - Regions
    - Availability Zones
    - Edge Locations

### What is AWS responsable for:

| Category                | Examples of AWS Services in the Category                                                                          | AWS Responsability                                                                                                            |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Infraestucture Services | Compute Services, such as Amazon Elastic Compute Cloud (Amazon EC2)                                               | AWS manages the underlying infrastructure and foundation services                                                             |
| Container Services      | Services that require less management from the customer, such Amazon Relational Database Service (Amazon RDS)     | AWS manages the underlying infrastructure and foundations services, operating system, and application platform                |
| Abstracted Services     | Services that require very little management from the customer, such as Amazon Simple Storage Service (Amazon S3) | AWS operates the infrastructure layer, operating system, and platforms, as well as server-side encryption and data protection |

### What is Customer responsable for:

| Category                | AWS Responsability                                                                                                            | Customer Responsability                                                                                                  |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Infrastructure services | AWS manages the infrastructure and foundation services                                                                        | You control the operating system and application platform, as well as encrypting, protecting, and managing customer data |
| Container Services      | AWS manages the infrastructure and foundation services, operating system, and application platform                            | You are responsible for customer data, encrypting that data, and protecting it through network firewalls and backups     |
| Abstracted Services     | AWS operates the infrastructure layer, operating system, and platforms, as well as server-side encryption and data protection | You are responsible for managing customer data and protecting it through client-side encryption                          |

### Resources

- [Shared Responsability Model](https://aws.amazon.com/compliance/shared-responsibility-model/)
