##### WHy organization move to the cloud

- Increase organizational agility
- Accelerate ability to innovate
- Strenghten security
- Reduce costs
- Operational expense versu capital investment

#### Twomodes for AWS storage services

- Consumed storage.
- Allocated capacity.

S3 are based on the amount of storage capacity that you conusme.

ES are based on the amount of capactiy that you allocate.

EFS you hae the option to use the default setting of consumed storage or provisioned storage.


#### Storage types

- Block

	Block Storage is raw storage in which the hardware storage device or drive is a disk or volume
	that is formatted and attached to the compute system for use. The blocks are the basic
	fixed storage units used to store data on the device.

	Can be HDD o SSD, Nvme, or san.

	Often shares management with an operating systems.

- File 

	Is built ontop of the block storage, typically serving as a file share of file server. File storage
	is created using an operating system that formats and manages the reading and writing of data to the block
	storage devices.

	SMB and NFS

- Object

	Is also built on top of block storage. Object storage is created using an operating system that formats and manages
	the reading and writing of data to the block storage devices. Object storage does not differentiate between 
	types of data. The type of data or the file becomes part of the data's metadata.

	Object storage is recognized for its inherent availibity of the file objects. Some systems support file versionsing,
	file tracking and file retention.



##### Storage fundamentals

	Block Storage: is a range of bytes or bits on a storage device. Block Storage files, are divided into blocks
	and written directly to empty blocks on a physical drive. Since blocks are assigned idenfifiers, they do need
	to be stored in adjacent sections of the disk.

	You can retrieve individual blocks separately from the rest of the file.
	Ideal for database


	File Storage: OS save data in hierarchical file system organized in the form of directories, sub-directories and files or folders
	When using a file-based system you must know the exactly path and location.



	Object Storage: Is a flat structure qhere the data called an object, is located in a single repository known as a bucket.
	In the user interface you could see the prefix like folder and subfoler, but the storage is still a flat structure.

#### 	Limits s3

	Up to 100 buckets per account
	You can't rename a bucket after creation
	After deleting a bucket the name becomes available for reuse by any account after 24 hours


#####   Keys

	When you create an object, you specify the key name. The key name uniquely identifies the object in the bucket. It is the full path
	to the object in the bucket.

#####   Versioning

	Versioning is a mens of keeping multiple variants of an object in the same bucket. You can use versioning to preserve, retrieve, and restore
	every version of every object stored in your amazon S3 bucket.
	Object can range in size from zero to 5 TB.

	You can control access to the objects you store in amazon s3. S3 supports both resource based and user-based access controls. ACL and bucket policies
	are both examples of resource-based access control.

##### Limitations upload files

	Using the console only 160 GB

	Per sdk , size up to 5 TB.

#####  Amazon s3 virtual-path [deprecated]

	https://<region>/<bucketname>/<object>

	ex: https://s3-us-west-2.amazon.com/getting-started-with-s3/dolphins.jpg

##### amazon s3 virtual-hosted

	Virtual hoting is the practice of serving multple websites from a single web server.
	https://<bucketname>.<region>/<object

	ex: https://getting-started-wit-s3.us-west-2.amazon.com/dolphin.jpg

##### Data transferr

-	AWS DATASYNC
	Makes it simple and fast to move large amounts of data online between on-premises
	storage and amazon s3. Data sync can transfers hunderds of terabytes and millions of files at speeds up to 10 times
	faster than open-source tools.

-       AWS TRANSFER FAMILY

	provides a fully managed support for file transfers directly into and out of amazon s3.   

-	AWS S3 transfer acceleration

	You can use Amazon S3 Transfer Acceleration for fast, easy, and secure transfers of files over long distances. It takes advantage of Amazon CloudFront globally distributed edge locati		ons, routing data to Amazon S3 over an optimized network path.

-       Amazon Kinesis Data Firehose
	You can also stream data into Amazon S3 by using Amazon Kinesis Data Firehose, a fully managed streaming service. 
        Because it captures and automatically loads streaming data in Amazon S3 and Amazon Redshift, you get near-real-time analytics with the business intelligence tools that you already use

-       Amazon Kinesis Data Streams (KDS) enables you to build custom applications that process or analyze streaming data for specialized needs. Kinesis Data Streams can continuously capture and store terabytes of data per hour from hundreds of thousands of sources, such as website clickstreams, financial transactions, social media feeds, IT logs, and location -tracking events. You can also emit data from Kinesis Data Streams to other AWS services, such as Amazon S3, Amazon Redshift, Amazon EMR, and AWS Lambda.

-     Amazon Partner Network
      You can use third-party connectors from the Amazon Partner Network for additional Amazon transfer service support. Amazon partners can help you move your data to the cloud. The simplest way to do that is through an embedded connection in your backup software. Using this approach, your backup catalog stays consistent so that you maintain visibility and controls across jobs that span disk, tape, and the cloud.
