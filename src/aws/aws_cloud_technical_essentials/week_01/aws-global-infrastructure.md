# AWS Global Infrastructure

## AWS Regions considerations

- Compliance (Regulations)
- Latency
- Pricing (may vary from region to region)
- Service availability

## AWS Global Infrastructure - Components

- Data Centers belong to -> Availability Zones belong to -> Regions
- Regions has -> Availability Zones has -> Data Centers
- Edge Locations

## Scope AWS Services:

- There are services with no request to specify the AZ, in this case AWS is responsable for increase data durability and availability, in the case you need to chose a AZ, it's your responsability to increase data durability and availability.

## Maintain Resiliency

- To keep your application available, you need to maintain high availability and resiliency. A well-known best practice for cloud arquitecture is to use Region-scoped, managed services, it's this not possible, make sure the workload is replicated across multiples AZ, at minimum you should use two AZ.

## Summary - AWS Global Infrastructure

- _Data Storage_: It's important to store employee photos safely, ideally using AWS to ensure accessibility and redundancy.
- _Redundancy_: AWS has multiple data centers organized into Availability Zones (AZs) and Regions to protect against data loss from disasters.
- _Choosing a Region_: When selecting an AWS region, consider:
- _Compliance_: Legal requirements for data location.
- _Latency_: Proximity to users for faster access.
- _Pricing_: Cost variations between regions.
- _Service Availability_: Ensure the required services are available in the chosen region.
- _Global Edge Network_: This includes Edge locations for caching content closer to users, reducing latency for global applications.

## Resources:

- [Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/)
- [AWS Global Infrastructure Documentation](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/global-infrastructure.html)
- [AWS Regions and Availability Zones](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/)
- [AWS Service Enpoints](https://docs.aws.amazon.com/general/latest/gr/rande.html)
- [AWS Regional Services](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/)

## Questions - Absolutely! Here are five practice questions based on the course content:

1. **True/False**: AWS uses redundancy to ensure that data is safe even if one data center fails.

2. **Multiple Choice**: What is the primary purpose of an Availability Zone (AZ) in AWS?

   - A) To provide a single point of failure
   - B) To cluster multiple data centers for redundancy
   - C) To store data only in one location
   - D) To limit access to data

3. **Open-Ended**: Describe the factors you should consider when choosing an AWS region for your application.

4. **Open-Ended**: How does latency affect the performance of applications hosted on AWS, and what can be done to mitigate it?

5. **True/False**: The Global Edge Network in AWS helps to reduce latency by caching content closer to end users.

## Responses

1. **True**: AWS uses redundancy to ensure that data is safe even if one data center fails.

2. **B) To cluster multiple data centers for redundancy**: An Availability Zone (AZ) is designed to provide redundancy and high availability.

3. **Factors to consider when choosing an AWS region**:

   - **Compliance**: Legal requirements for data location.
   - **Latency**: Proximity to users for faster access.
   - **Pricing**: Cost variations between regions.
   - **Service Availability**: Ensure the required services are available in the chosen region.

4. **Latency affects performance** by increasing the time it takes for data to travel between the user and the server. To mitigate it, you can use Edge locations to cache frequently accessed content closer to users.

5. **True**: The Global Edge Network in AWS helps to reduce latency by caching content closer to end users.

## Convention name and codes for regions

- Northern Virginia Region, is a region located in Northern Virginia
- US East (N. Virginia) is us-east-1
