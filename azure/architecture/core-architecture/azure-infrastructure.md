
# Azure Infrastructure

Azure's architecture consists of two groups:
- Physical infrastructure
- Management infrastructure

# Physical Infrastructure

Physical infrastructure includes datacenters, regions, and zones.

Individual datacenters are not accessible. They are grouped into Azure Regions *(or Azure Availability
Zones)* that you can access.

## Azure Regions

Azure Region:

> Area that contains one or several data centres that are geographically close and networked together.

The resources within the area are controlled to meet workloads.

When deploying a resource, you must decide which region the resource is deployed in.

> Some services are only available in specific regions. This can be certain VM sizes, or storage types.

> Some services do not require you to select a region.

## Availability Zones

![[availability-zones.png]]

Availability Zones:

> Zones are physically separate data centres in an Azure Region.

Each zone consists or 1 or more independent data centres. If one zone goes down, the other zones
continue working.

All zones are interconnected.

> All Azure Regions have at least 3 separate availability zones to ensure reliability and up-time.

**Usage in Apps:**

Availability Zones provide redundancy for your information. They can be used to run important services,
ensuring high-availability.

Availability Zones are primarily for:
- VMs
- Managed disks
- SQL databases

Services that use zones have 3 categories:
- Zonal services -
	- **Resource is pinned to a specific zone**
	- *VMs, managed disks, IPs*
- Zone-redundant services
	- **Platform replicates across zones**
	- *Zone-redundant storage, SQL databases*
- Non-regional services 
	- **Services always available even with zone-wide and region-wide outages**

## Region Pairs

![[region-pairs.png]]

Azure regions are paired with another region at least 300 miles away.

> This prevents interruptions from natural disasters, power outages, civil unrest, etc.

Most regions are two-way paired. The regions provide backups for each-other.
**However,** some regions provide only one-direction pairing, instead relying on a line of regions.

## Sovereign Regions

Sovereign regions:

> Instances of Azure isolated from the main Microsoft instance.

*These are used for legal reasons.*

Examples:
- US DoD, US Gov - 
	- **Regions have physical and network isolation**
	- *Operated by screened personnel*
- China East, China North
	- **Microsoft does not maintain the data centres**

# Management Infrastructure

Management infrastructure includes:
- Azure resources
- Resource groups
- Subscriptions
- Accounts

## Azure Resources & Resource Groups

**Resources,**

> Basic building block of Azure. Anything you create, provision, deploy is a resource.

Resources include:
- Virtual machines
- Databases
- Cognitive services

**Resource groups,**

> Grouping of resources. When a resource is created, it must be placed into a resource group.

Resource groups have a one-to-many relationship with resources.

> A single resource group can have many resources.
/
> A resource can not be in multiple groups.

Moreover, resource groups can not be nested.

Performing an action on a resource group, performs the action on all the resources inside it.

**Example:** Setting up a temporary development environment

- Grouping the resources
- De-provision all resources at once by removing the resource group
- Provisioning, several different access schemas, group based on access schemas, assign groups access

## Azure Subscriptions

![[subscriptions.png]]

Azure subscriptions are a unit of management, billing and scale.

> Allow you to logically organise resource groups and facilitate billing

To use Azure, you must use have a subscription.

> Subscriptions provide you with access to Azure products and services. This allows you to provision
  resources.

Azure subscriptions link to Azure accounts, which is an identity in Azure Active Directory.

Accounts can have multiple subscriptions. Subscriptions can be used to configure different billing
models and use different access policies.
- Billing boundary - Determines how an Azure account is billed. Different subscriptions for
  different types of billing requirements. Separate billing reports are generated for each
  subscription.
- Access control boundary - Implement access management at the subscription level. Different departments
  have different subscription policies.

**Examples:**
- Environments
    - Different subscriptions for development and testing, or data isolation
- Organisational Structuring
    - Teams can have different resources made available to them
    - IT department can have full range
    - HR could have less resources
- Billing
    - Separate billing
    - Separate subscriptions for testing, development, and production.

## Azure Management Groups

![[management-groups.png]]

Resources are gathered into resource groups, resource groups are gathered into subscriptions,
subscriptions are gathered into management groups.

Like resource groups and subscriptions, management groups have inheritance.
However, a major difference is that management groups can be nested.
