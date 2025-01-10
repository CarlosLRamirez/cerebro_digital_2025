---
created: 2024-12-30T20:43:18
modified: '"2024-12-30 20:44", "1tc/G12T+6"'
type: 
aliases: 
tags:
  - AWS
---


# 04-IAM, ACCOUNTS AND AWS ORGANISATIONS

## IAM Identity Policies
- Also known and policy documents
- written in JSON
- A series of Statements
	- Sid (optional) - recommended
	- Action - what are you trying to do, you can use wildcards or a list of actions
	- Resource - you can use wildcards or a list of resources (ARN format)
	- Effect - Allow or Deny
- Statements evaluation priority order
	1. Explicit DENY
	2. Explicit ALLOW
	3. Default DENY (Implicit)
- All IAM identities (excluding the account root) have any default permissions, whatsoever.
- There are two main type of policies:
	- Inline policies
	- Managed policies. (Reusable, Low Management Overhead)
- There are two types of Managed policies
	- AWS Managed policies
	- User Managed policies
-

## IAM Users
- `IAM Users` are identity used for anything requiring **long-term** AWS access. e.g. **Humans, Applications** or **service accounts**  (a named, identified thing)
- Identity of IAM Users are done using, either:
	- Username and password
	- Access Keys
- Amazon Resource Name (ARN)
	- Uniquely identify resources within any AWS accounts
- you can only have **5,000** IAM Users **per account**
- IAM Users can be member of **10** groups.
- 3dfajdñfkjañdlf
- añldkjfñlakjs
- ñlasjñdflk
- ñalskjdfa
- ñlajsdñlfkjas
- ñlaksjdñflkasd
- ñlkjñl
- 