# A Look into AWS Data Services

In this course, the Morgan and Raf cover some of the AWS data services that can be used for a solution that ingests clickstream data. Clickstream is the term for small events that contain pieces of data that are generated continuously with high speed and volume. Remember, clickstream data is usually data that’s collected by systems (mostly frontends) regarding user interactions with that system. In this week’s scenario, clickstream data will be used to collect information about users’ behaviors when they interact with a restaurant menu. Regardless of whether you are architecting for clickstream data, AWS provides various analytics services that meet your needs for data analytics. Organizations of all sizes and industries can use these services to reinvent their business with data.

## AWS data services

From data movement, data storage, data lakes, big data analytics, log analytics, streaming analytics, business intelligence, and machine learning (ML) to many things in between, AWS offers purpose-built services that provide price performance, scalability, and low costs. [Data Lakes and Analytics on AWS](https://aws.amazon.com/big-data/datalakes-and-analytics/) lists all the AWS services that can be used for data analytics, and places the services into four distinct categories. This reading summarizes the most popular services in each category.

## Data lakes and data storage

#### Amazon S3

Amazon Simple Storage Service (Amazon S3) is an object storage service that offers scalability, data availability, security, and performance. Customers of all sizes and industries can store and protect virtually any amount of data for virtually any use case, such as data lakes, cloud-native applications, and mobile apps. With cost-effective storage classes and easy-to-use management features, you can optimize costs, organize data, and configure fine-tuned access controls to meet specific business, organizational, and compliance requirements.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xpDo1_CATs6a3dnaA9cVzA_4b9ae8b78cb3407baf58440f97a67cf1_Reading2.1A.png?expiry=1745020800000&hmac=q3GALnpITfOUuYCHOt7ROBy7bdIFL5BMWa9TUkocoQ4)

The following list details some use cases for Amazon S3:

-   Archive data at the lowest cost: Move data archives to the Amazon Simple Storage Service Glacier (Amazon S3 Glacier storage classes to lower costs, reduce operational complexities, and gain new insights.
-   Run cloud-native applications: Build fast, powerful, mobile and web-based cloud-native applications that scale automatically in a highly available configuration, such as static websites that use the client side for coding.
-   Build a data lake: Run big data analytics, artificial intelligence (AI), machine learning (ML), and high performance computing (HPC) applications to unlock data insights.
-   Back up and restore critical data: Meet Recovery Time Objectives (RTO), Recovery Point Objectives (RPO), and compliance requirements with the robust replication features of Amazon S3.

For more information, see [Amazon S3](https://aws.amazon.com/s3/).

#### Amazon S3 Glacier

**Note:** Amazon S3 storage classes will have their own dedicated reading later in this week.The Amazon S3 Glacier storage classes are purpose-built for data archiving. They are designed to provide you with high performance, retrieval flexibility, and low-cost archive storage in the cloud. All S3 Glacier storage classes provide virtually unlimited scalability and are designed for 99.999999999 percent (11 nines) of data durability. In addition to low-cost storage, the S3 Glacier storage classes also deliver options for fast access to your archival data.

For more information, see [Amazon S3 Glacier storage classes](https://aws.amazon.com/s3/storage-classes/glacier/).

#### AWS Lake Formation

AWS Lake Formation is a service that you can use to set up a secure data lake in days. A data lake is a centralized, curated, and secured repository that stores all your data, both in its original form and prepared for analysis. You can use a data lake to break down data silos and combine different types of analytics to gain insights and guide better business decisions.

For more information, see [AWS Lake Formation](https://aws.amazon.com/lake-formation/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc).

## Data analytics

#### Amazon Athena

Amazon Athena is an interactive query service that you can use to analyze data in Amazon S3 by using standard Structured Query Language (SQL). Athena is serverless, so you don’t need to manage infrastructure, and you pay only for the queries that you run.

Using Athena is straightforward. You point to your data in Amazon S3, define the schema, and start querying by using standard SQL. Most results are delivered within seconds. With Athena, you don’t need complex extract, transform, and load (ETL) jobs to prepare your data for analysis. Anyone with SQL skills can use Athena to quickly analyze large-scale datasets.

For more information, see [Amazon Athena](https://aws.amazon.com/athena/).

#### Amazon EMR

Amazon EMR is a big data solution for petabyte-scale data processing, interactive analytics, and machine learning that use open-source frameworks, such as Apache Spark, Apache Hive, and Presto.

In this course, we didn’t use or explore Amazon EMR for this week’s scenario because the customer was short-staffed, and Amazon EMR requires a learning curve to operate the open-source frameworks that it uses. In fact, Amazon EMR has so many features that we could make an entire 4-week course about it! The following list details some of the use cases for Amazon EMR. (Notice that the third item aligns well with the week’s scenario—Amazon EMR would a good candidate for the task if the customer already had big data knowledge.)

-   Run large-scale data processing and what-if analysis by using statistical algorithms and predictive models to uncover hidden patterns, correlations, market trends, and customer preferences.
-   Extract data from various sources, process it at scale, and make the data available for applications and users.
-   Analyze events from streaming data sources in real time to create long-running, highly available, and fault-tolerant streaming data pipelines.
-   Analyze data using open-source ML frameworks, such as Apache Spark MLlib, TensorFlow, and Apache MXNet.
-   Connect to Amazon SageMaker Studio for large-scale model training, analysis, and reporting.

For more information, see [Amazon EMR](https://aws.amazon.com/emr/?c=a&sec=srv).

#### Amazon OpenSearch Service

You can use Amazon OpenSearch Service to perform interactive log analytics, real-time application monitoring, website search, and more. OpenSearch is an open source, distributed search and analytics suite that is derived from Elasticsearch. Amazon OpenSearch Service is the successor to Amazon Elasticsearch Service. It offers the latest versions of OpenSearch, support for 19 versions of Elasticsearch, and visualization capabilities that are powered by OpenSearch Dashboards and Kibana. Amazon OpenSearch Service currently has tens of thousands of active customers, with hundreds of thousands of clusters under management, processing hundreds of trillions of requests per month.

For more information, see [Amazon OpenSearch Service](https://aws.amazon.com/opensearch-service/?c=a&sec=srv).

## Data movement

#### Amazon Kinesis

**Note:** Later this week, Amazon Kinesis will have its own dedicated reading that further explains each of the Kinesis services (such as Amazon Kinesis Data Streams, Amazon Kinesis Data Firehose, and Amazon Kinesis Data Analytics).

With Amazon Kinesis, you can collect, process, and analyze real-time, streaming data so that you can get timely insights and react quickly to new information. Amazon Kinesis offers key capabilities to cost-effectively process streaming data at virtually any scale, along with the flexibility to choose the tools that best suit the requirements of your application. With Amazon Kinesis, you can ingest real-time data such as video, audio, application logs, website clickstreams, and Internet of Things (IoT) telemetry data for machine learning, analytics, and other applications. You can use Amazon Kinesis to process and analyze data as it arrives, which means that you can respond quickly—you don’t need to wait for all your data to be collected before processing can begin.

For more information, see [Amazon Kinesis](https://aws.amazon.com/kinesis/).

#### AWS Glue

AWS Glue is a serverless data integration service that you can use to discover, prepare, and combine data for analytics, machine learning, and application development. AWS Glue provides capabilities that are needed for data integration so that you can start analyzing your data and using your data in minutes instead of months. Data integration is the process of preparing and combining data for analytics, machine learning, and application development. It involves multiple tasks, such as discovering and extracting data from various sources; enriching, cleaning, normalizing, and combining data; and loading and organizing data in databases, data warehouses, and data lakes. These tasks are often handled by different types of users who each use different products.

For more information, see [AWS Glue](https://aws.amazon.com/glue/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc).

#### AWS DMS

AWS Database Migration Service (AWS DMS) helps you migrate databases to AWS quickly and securely. The source database remains fully operational during the migration, which minimizes downtime to applications that rely on the database. AWS DMS can migrate your data to and from the most widely used commercial and open-source databases.

For more information, see [AWS Database Migration Service](https://aws.amazon.com/dms/).

## Predictive analytics and machine learning

You won’t explore this area much in this course, but—as was mentioned earlier in this reading—regardless of the kind of architecture you want to create, AWS offers services that can help. (That is, use the right tool for the job!) Though you might not see the following AWS services typically listed with AWS data services, you can use them to handle or process data for predictive analytics and machine learning (ML).

#### Amazon SageMaker

SageMaker can be used for any generic ML solution. You can use it to build, train, and deploy ML models for virtually any use case with fully managed infrastructure, tools, and workflows. SageMaker requires a learning curve to use, but it’s a managed serverless service that many people can use to innovate with ML through a choice of tools—such as integrated development environments (IDEs) for data scientists and no-code interfaces for business analysts.

For more information, see [Amazon SageMaker](https://aws.amazon.com/sagemaker/).

#### Amazon Rekognition

Amazon Rekognition is one of Raf’s favorite ML services from the entire list of AWS services! It is easy to use, serverless, and abstracted, in the sense that you interact with it by doing API calls. With Amazon Rekognition, you can automate image and video analysis by adding pretrained or customizable computer vision API operations to your applications without building ML models and infrastructure from scratch.

On its own, Amazon Rekognition is not a data analytics service. However, it’s listed here because you can use it as part of a data analytics solution. It is designed to analyze millions of images, streaming, and stored videos within 3 seconds.

Check out some examples:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/iy_zfA01SPOvZs1T1q-ljA_8a172adfbded4d16859daba3a5e374f1_Reading2.1B.png?expiry=1745020800000&hmac=daL35_-8oeB9W2a0d-2nTWQtWWwJHXS0hcGOvsN2XQ4)

In this image, Amazon Rekognition is detecting objects (such as packages, pets, or people) in real time from live video streams.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/i6P1guYnTMO1YfyQUNhl2A_d36554b65f794cd2bdaf6a41048462f1_Reading2.1C.png?expiry=1745020800000&hmac=JBMnZsG818Gq8aFEhFKRUnk71aTHgcWRSQtKNZTswR4)

In this image, Amazon Rekognition is detecting faces that appear in images and videos, and recognizing attributes (such as open eyes, glasses, and facial hair) for each face.

For more information, see [Amazon Rekognition](https://aws.amazon.com/rekognition/).

#### Amazon Comprehend

Amazon Comprehend is a natural-language processing (NLP) service that uses ML to uncover valuable insights and connections in text, which is instrumental for a data analytics solution. For example, you could mine business and call center analytics or process financial documents. For medical use cases, you can use Amazon Comprehend Medical, which focuses on extracting information accurately and quickly from unstructured medical text.For more information, see [Amazon Comprehend](https://aws.amazon.com/comprehend/) and [Amazon Comprehend Medical](https://aws.amazon.com/comprehend/medical/).
