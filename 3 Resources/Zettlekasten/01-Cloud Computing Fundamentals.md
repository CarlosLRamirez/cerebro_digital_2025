---
created: 2024-12-30T20:42:17
modified: '"2024-12-30 20:44", "1tc/G12T+6"'
type: 
aliases: 
tags:
  - AWS
---

# 01-Cloud Computing Fundamentals

- Cloud Computing characteristics (as per NIST)
	- On-Demand Self-Service
	- Broad Network Access
	- Resource Pooling
	- Rapid Elasticity
	- Measured Service

- On-Demand Self-Service, as a feature of a Cloud Computing service
	- "can provision capabilities as needed **without requiring human interaction**"                                                                                                                                            
- Broad Network Access, as a feature of a Cloud Computing service
	- "Capabilities are available over the **network** and accessed through **standard mechanisms**.                                                                                                                    
- Resource Pooling, as a feature of a Cloud Computing service
	- "There is a sense of **location independence**... no **control** or **knowledge** over the exact **location** of the resources" "... Resources are pooled to server multiple consumers using a multi-tenant model (economies of scale)".

- Rapid Elasticity, as a feature of a Cloud Computing service
	- "Capabilities can be **elastically provisioned** and **released** to scale **rapidly** outward and inward with demand" "To the consumer, the capabilities available for provisioning often **appear** to be **unlimited**" 

- Measured Service, , as a feature of a Cloud Computing service
	- "Resource usage can be **monitored**, **controlled**, **reported**... AND **BILLED**"

- Public Cloud
	- A Cloud platform that is available to the general public

- Multi Cloud
	- When you use multiple public cloud providers on your application. (AWS + Azure, etc..)

- Private Cloud (On-premises)
	- When you have Public Cloud Hardware but located on your premise (i.e. AWS Outpost)

- On-premises infrastructure
	- VMWare, HyperV
	- Is **not** private cloud

- Hybrid Cloud
	- When you use Public Cloud and Private Cloud (On-premises) together (example: AWS + AWS Outpost) 
	- Is **NOT** when you use AWS together with your legacy on-premises (VMware)

- Hybrid Environment
	- When have Public/Private Cloud together with your On-Premise stuff (VMware etc..) 

- Generic infrastructure stack (Tiers), every application needs: 
	- Application
	- Data
	- Runtime
	- Container
	- O/S
	- Virtualization
	- Servers
	- Infrastructure
	- Facilities

-  Unit of consumption
	- The part of the stack that you consume
	- The part of the system where from that point upwards in the infrastructure stack you are responsible of management.

- Infrastructure as a Service (IaaS)
	- You manage the O/S (unit of consumption)
	- You abstract the virtualization and everything downwards
	- i.e. EC2 instances

- Platform as a Service (PaaS)
	- You consume the runtime environment to run your application
	- i.e. Heroku, AWS Beanstalk

- Software as a Service (SaaS)
	- You consume the application
	- You abstract everything else
	- i.e. Office 365, Google Workspace, Netflix, etc..
 
