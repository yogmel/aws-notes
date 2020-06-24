# AWS Notes

- [Open Reference](https://github.com/open-guides/og-aws);

# Basics
## AWS Regions

- [Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/);
- [Check services for each Region](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/?p=ngi&loc=4);

AWS has regions all around the world (check link to full list of locations) and each location has a name. A region is a **cluster of data centers** and some services are **region-scoped**, others are **global**.

Example of region name: sa-east-1 (South America, Sao Paulo)

## Avaliability Zones (AZ)
Each region have many availability zones (from 2 to 6, usually 3). They are discrete data centers with redundant power, networking, and connectivity, physically isolated from each other. This is good in case a disaster disables one of them.

They are still connected with high bandwidth, low latency newtworking.

Example of AZ name: sa-east-1a, sa-east-1b, sa-east-1c.

----

## Identity and Access Management (IAM)
Scope: global

Manages the overall security in the AWS account. It controls:
- Users: usually a physical person
- Groups: by function, by team and it contain users
- Roles: grouping for internal usage

After the first login, the *root* account should **never** be used again. Also, it is best to give users the minimal of permission they need (least privilege principles).

Root user: _username_
Non-root user: _username @ account-name_

Some specs:
- Policies (what users can or cannot do) are written in JSON. There are predefined "managed policies"
- MFA (multi factor authentication) can be setup
