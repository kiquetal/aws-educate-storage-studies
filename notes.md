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

