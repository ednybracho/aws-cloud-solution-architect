# Amazon S3 Cross-Region Replication and Object Lifecycle

## S3 CRR

With S3 Cross-Region Replication (CRR), you can replicate objects—and their respective metadata and object tags—into other AWS Regions for reduced latency, compliance, security, disaster recovery, and other use cases. CRR can be configured from a single, source Amazon Simple Storage Service (Amazon S3) bucket to replicate objects into one or more destination buckets in another AWS Region.

CRR automatically replicates data between buckets across different AWS Regions. With CRR, you can set up replication at a bucket level, a shared prefix level, or an object level (by using Amazon S3 object tags).

You can use CRR to provide lower-latency data access in different geographic regions. CRR can also help if you have a compliance requirement to store copies of data hundreds of miles apart. You can use CRR to change account ownership for the replicated objects to protect data from accidental deletion. For more information about CRR, see [Replicating objects](https://docs.aws.amazon.com/AmazonS3/latest/userguide/replication.html) in the _Amazon S3 User Guide_.

Example use cases include the following:

-   Compliance: Amazon S3 stores your data across multiple geographically distant Availability Zones by default. However, compliance requirements might require you to store data at even greater distances. You can use CRR to replicate data between distant AWS Regions to satisfy these requirements.
-   Latency performance: If your customers or end users are distributed across one or more geographic locations, you can minimize latency for data access by maintaining multiple object copies in AWS Regions that are geographically closer to your customers.
-   Regional efficiency: If you have compute clusters in two or more AWS Regions that analyze the same set of objects, you might choose to maintain object copies in all of those AWS Regions.

## S3 Lifecycle

You can add rules in an S3 Lifecycle configuration to tell Amazon S3 to transition objects to another Amazon S3 storage class. For more information about storage classes, see. Some examples of when you might use S3 Lifecycle configurations in this way include the following:

-   When you know that objects are infrequently accessed, you might transition them to the S3 Standard-IA storage class.
-   You might want to archive objects that you don't need to access in real time to the S3 Glacier Flexible Retrieval storage class.

However, what if you’re not sure about the data access patterns?

### Amazon S3 Intelligent-Tiering storage class

S3 Intelligent-Tiering is a good storage class for data with unknown, changing, or unpredictable access patterns—independent of object size or retention period. You can use S3 Intelligent-Tiering as the default storage class for virtually any workload, especially data lakes, data analytics, new applications, and user-generated content.

S3 Intelligent-Tiering is the only cloud storage class that’s designed to deliver automatic storage cost savings when data access patterns change, without performance impact or operational overhead. S3 Intelligent-Tiering is designed to optimize storage costs by automatically moving data to the most cost-effective access tier when access patterns change. For a small monthly object monitoring and automation charge, S3 Intelligent-Tiering monitors access patterns and automatically moves objects that haven’t been accessed to lower-cost access tiers.

There are no retrieval charges in S3 Intelligent-Tiering. S3 Intelligent-Tiering has no minimum eligible object size, but objects smaller than 128 KB are not eligible for automatic tiering. These smaller objects can be stored, but they will always be charged at the Frequent Access tier rates and don’t incur the monitoring and automation charge.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/D8fzzMCvRVyI7RdBJLkFTw_7951069382b045c994fbac7ac76f4ff1_Reading2.2A.png?expiry=1745107200000&hmac=JE0j8zAPiKfgNSbX5HrS6MbZOF51hNkibIcpdumspQk)

For more information, see [Amazon S3 Intelligent-Tiering storage class](https://aws.amazon.com/s3/storage-classes/intelligent-tiering/).

### Amazon S3 Glacier storage classes

You can use Amazon S3 Lifecycle policies to transition objects from one storage class to another. These storage classes include Amazon Simple Storage Service Glacier (Amazon S3 Glacier) storage classes, which are purpose-built for data archiving. S3 Glacier storage classes provide you with low-cost archive storage in the cloud. All S3 Glacier storage classes provide virtually unlimited scalability and are designed for 99.999999999 percent (11 nines) of data durability. The S3 Glacier storage classes deliver options for fast access to your archive data and low-cost archive storage in the cloud.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/8lPIyU4NRyKS1l0B0okGOQ_b48af64b58f843caada35f01685a0cf1_Reading2.2B.png?expiry=1745107200000&hmac=340YBc25PuXtkMYk_D655l5HOBS5S-7qMmM4V0cnRis)

For more information, see [Amazon S3 Glacier storage classes](https://aws.amazon.com/s3/storage-classes/glacier/).
