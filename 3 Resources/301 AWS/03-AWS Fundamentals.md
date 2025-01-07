---
created: 2024-12-30T20:43:01
modified: '"2024-12-30 20:44", "1tc/G12T+6"'
type: 
aliases: 
tags:
  - AWS
---







[[Elastic Compute Cloud (EC2) Basics]]

## S3 Basics
### S3 101
- Global Storage Plataform - regional based/resilent
- S3 is a Public service, unlimited data & multi-user
- S3 can be accessed via
	- UI
	- CLI
	- API
	- HTTP
- S3 main elements:
	- Object
	- Buckets

### S3 Objects
- S3 Object main two componentes
	- Key = think like the file name
	- Value =Content being stored
- S3 Objects size can be `Zero byte to 5 TB`
- Another components for an S Object
	- Vesion ID
	- Metadata
	- Access Control
	- Subresources
### S3 Buckets
- S3 is a Global based services, however when you create an S3 Buckets you have to select an specific AWS region.
	- True
- The data inside a S3 Bucket has a primary home region
- Data never leaves that region, unless you configure it.
- S3 buckets Blast Radius = `Region` 
- S3 Bucket names are Globally Unique
- An S3 Buckets could have unlimited objects
- S3 Buckets have flat structure, it not a file system with folders and subfolders
- Even the UI present the data in folders, it is a flat structure, what happen is that object keys are like this: */folder/Koala1.jpg*
- folders are commonly reffered as `prefixes` of S3 objects

### Summary
- Bucket names are **globally unique**
	- Yes
- S3 Bucket names limitations
	- 3-63 characters, all lower case, no underscores
	- Start with a lowercase letter or a number
	- Can't be IP formated
- S3 Bucket quantity limitations 
	- 100 soft bucket limits per AWS account
	- 1000 hard bucket limit  per AWS account
- Unlimited object in bucket, 0 bytes to 5TB
- Key = Name, Value = Data

### S3 Patterns and Anti-Patterns
- S3 is an object store - not file or block
- You CAN'T MOUNT an S3 bucket on Windows or Linux.
- Great for large scale data storage, distribution or upload
- Great of 'offload'
- INPUT and/or OUTPUT to MANY AWS products
- S3 buckets are not public accessible by default


## Cloud Formation Basics
### The basics
- It uses templates writen in
	- YAML
	- JSON
- The only mandatory part of a template is:
	- A list of resources
- ***Description*** must directly follow ***AWSTemplateFormatVersion*** on a YAML Cloud formation template
- AWSTemplateFormat Version
	- the way that AWS allow for extending the standard over time
- Metadata, controls how the template will be shown on the UI
- Another elements of CloudFormation templates
	- Parameters, prompt user for information.
	- Mappings 
	- Conditions
	- Transform
	- Outputs
- Resources in CloudFormation templates are logical resources
- A stack (or stacks) or logical resoureces is created from a teomplate, then converted to physical resources
- CloudFormation keeps sync between the stack and the physical resources

## Route53 (R53) Fundamentals
- Global-based service
	- Globally Resillient
- 2 main services
	- Register Domains
	- Host Zones... managed nameservers
- Host Zones 
	- Zone files in AW
	- Hosted in our managed name servers
	- Can be public or private (linked to VPC(s))
	- stores records (recorsets)
- AWS is the registar
- .COM, .ORG, .IO etc, TLD are the registry