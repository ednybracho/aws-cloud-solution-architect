# AWS Global Infrastructure

## AWS Regions considerations

-   Compliance (Regulations)
-   Latency
-   Pricing (may vary from region to region)
-   Service availability

## AWS Global Infrastructure - Components

-   Data Centers belong to -> Availability Zones belong to -> Regions
-   Regions has -> Availability Zones has -> Data Centers
-   Edge Locations

## Scope AWS Services:

-   There are services with no request to specify the AZ, in this case AWS is responsable for increase data durability and availability, in the case you need to chose a AZ, it's your responsability to increase data durability and availability.

## Maintain Resiliency

-   To keep your application available, you need to maintain high availability and resiliency. A well-known best practice for cloud arquitecture is to use Region-scoped, managed services, it's this not possible, make sure the workload is replicated across multiples AZ, at minimum you should use two AZ.

## Summary - AWS Global Infrastructure

-   _Data Storage_: It's important to store employee photos safely, ideally using AWS to ensure accessibility and redundancy.
-   _Redundancy_: AWS has multiple data centers organized into Availability Zones (AZs) and Regions to protect against data loss from disasters.
-   _Choosing a Region_: When selecting an AWS region, consider:
-   _Compliance_: Legal requirements for data location.
-   _Latency_: Proximity to users for faster access.
-   _Pricing_: Cost variations between regions.
-   _Service Availability_: Ensure the required services are available in the chosen region.
-   _Global Edge Network_: This includes Edge locations for caching content closer to users, reducing latency for global applications.

# AWS Global Infrastructure

Infrastructure, like data centers and networking connectivity, still exists as the foundation of every cloud application. In AWS, this physical infrastructure makes up the AWS Global Infrastructure, in the form of Availability Zones and Regions.

## REGIONS

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/GA-td82sSJ-A1bMhZAK-Kg_76e9d578334d47e6b9f7a74ec2376bf1_Regions.png?expiry=1742256000000&hmac=h1zjNCBprpvDGIrSAip_1X8a1sTqkLZlseodMVOG_QQ)

Regions are geographic locations worldwide where AWS hosts its data centers. AWS Regions are named after the location where they reside. For example, in the United States, there is a Region in Northern Virginia called the Northern Virginia Region and a Region in Oregon called the Oregon Region. There are Regions in Asia Pacific, Canada, Europe, the Middle East, and South America, and AWS continues to expand to meet the needs of its customers.Each AWS Region is associated with a geographical name and a Region code.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/hDx5s-sZRkGvR_XA-VoZ2A_57b85de84aed4ee9be064082687493f1_image.png?expiry=1742256000000&hmac=ykfQs2gjKSRY6ph85IuVHAj6XCr0Eue_dZYqR7DIA6M)

Here are a few examples of Region codes:

-   us-east-1: This is the first Region created in the east of the US. The geographical name for this Region is N. Virginia.
-   ap-northeast-1: The first Region created in the northeast of Asia Pacific. The geographical name for this Region is Tokyo.

AWS Regions are independent from one another. This means that your data is not replicated from one Region to another, without your explicit consent and authorization.

## CHOOSE THE RIGHT AWS REGION

Consider four main aspects when deciding which AWS Region to host your applications and workloads: latency, price, service availability, and compliance.

**Latency.** If your application is sensitive to latency, choose a Region that is close to your user base. This helps prevent long wait times for your customers. Synchronous applications such as gaming, telephony, WebSockets, and IoT are significantly affected by higher latency, but even asynchronous workloads, such as ecommerce applications, can suffer from an impact on user connectivity.

**Price.** Due to the local economy and the physical nature of operating data centers, prices may vary from one Region to another. The pricing in a Region can be impacted by internet connectivity, prices of imported pieces of equipment, customs, real estate, and more. Instead of charging a flat rate worldwide, AWS charges based on the financial factors specific to the location.

**Service availability.** Some services may not be available in some Regions. The AWS documentation provides a table containing the Regions and the available services within each one.

**Data compliance.** Enterprise companies often need to comply with regulations that require customer data to be stored in a specific geographic territory. If applicable, you should choose a Region that meets your compliance requirements.

## AVAILABILITY ZONES

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/lIc5YSi_SuCX4wI4pGNmsg_b3dde14493c846fdbd18a10956d6b3f1_AZs.png?expiry=1742256000000&hmac=RUVBZdRAAJu4OBQsB3A76XcsauQQG9DkkMgs6j7EiL4)

Inside every Region is a cluster of Availability Zones (AZ). An AZ consists of one or more data centers with redundant power, networking, and connectivity. These data centers operate in discrete facilities with undisclosed locations. They are connected using redundant high-speed and low-latency links.AZs also have a code name. Since they’re located inside Regions, they can be addressed by appending a letter to the end of the Region code name. For example:

-   us-east-1a: an AZ in us-east-1 (Northern Virginia Region)
-   sa-east-1b: an AZ in sa-east-1 (São Paulo Region in South America)

If you see that a resource exists in us-east-1c, you know this resource is located in AZ c of the us-east-1 Region.

## SCOPE AWS SERVICES

Depending on the AWS Service you use, your resources are either deployed at the AZ, Region, or Global level. Each service is different, so you need to understand how the scope of a service may affect your application architecture.When you operate a Region-scoped service, you only need to select the Region you want to use. If you are not asked to specify an individual AZ to deploy the service in, this is an indicator that the service operates on a Region-scope level. For region-scoped services, AWS automatically performs actions to increase data durability and availability.On the other hand, some services ask you to specify an AZ. With these services, you are often responsible for increasing the data durability and high availability of these resources.

## MAINTAIN RESILIENCY

To keep your application available, you need to maintain high availability and resiliency. A well-known best practice for cloud architecture is to use Region-scoped, managed services. These services come with availability and resiliency built in.When that is not possible, make sure the workload is replicated across multiple AZs. At a minimum, you should use two AZs. If one entire AZ fails, your application will have infrastructure up and running in at least a second AZ to take over the traffic.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/3ToUyNl3TKScMGwOy5hFTA_7273fe75dd8941b8a6f8644d419a16f1_image.png?expiry=1742256000000&hmac=oob85e8In2URBYNpULOymcJyctsVGXprY5Eoq2JUyPM)

## Resources:

-   [Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/)
-   [AWS Global Infrastructure Documentation](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/global-infrastructure.html)
-   [AWS Regions and Availability Zones](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/)
-   [AWS Service Enpoints](https://docs.aws.amazon.com/general/latest/gr/rande.html)
-   [AWS Regional Services](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/)

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

-   Northern Virginia Region, is a region located in Northern Virginia
-   US East (N. Virginia) is us-east-1
