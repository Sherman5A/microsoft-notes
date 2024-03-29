
# Azure Costs

Cost of Azure depends on the resources you use.

Expenditure depends on:
- Resource type
- Consumption
- Maintenance
- Geography
- Subscription type
- Azure Marketplace

Azure offers many tools to estimate costs,

- Total Cost Ownership (TCO) calculator compares the cost of operating through Azure to operating on-premises
    - Input resources and services
    - Adjust costs based on location and organisation
    - Report is generated that estimates costs
- Pricing Calculator which recommends Azure services that fit your budget
    - Estimates cost of provisioning resources
- Azure Adviser
    - Monitors actual costs
    - Can limit spending
    - Provides recommendations

## Resource Type

Type of resources, resource settings, Azure region impact costs.

When provisioning a resource, Azure creates a metered instance. This tracks the resource's usage.

**Example: Storage Account**

![[blob-storage.png]]

Specify,
- Type
- Performance tier
- Access tier
- Redundancy settings
- Region

**Example: Virtual Machine**

![[virtual-machine-settings.png]]

Specify,
- OS licensing
- Processor
- Number of cores
- Attached storage
- Network interface
- Region

## Consumption

Using more computer resources, mean you pay more.

Alternative, pay for resources in advance, and receive discounts on reserved resources up to 72%.

## Maintenance

Provisioning a VM provisions additional resources such as storage and networking. When the VM is
de-provisioned those additional resources may not de-provision at the same time.

## Geography

Regions have different costs depending on region's labour, taxes, and fees.

## Network Traffic

Billing zones determine cost of outbound data transfers. Inbound data transfers are free.

## Subscription Type

Azure subscriptions provide usage allowances.

## Azure Marketplace

Allows you to purchase Azure-based solutions and services from 3rd party vendors.

This can be server with software preinstalled, or managed network firewalls.

You have to pay for the Azure services, and also the 3rd party vendors service expenses.

# Azure Cost Management Tool

Allows you to quickly check resource costs, create alerts for the resource spending, and create budgets
for automated resource management.

Cost analysis view provides a visual of all Azure costs.

**Budget Alerts**

Alert you when spending exceeds a condition set in the budget. This can be through upright cost,
or usage costs.

**Credit Alerts**

Notifies you when Azure credits  are consumed. Alerts are generated at 90% and 100% of credit balance.

**Department Spending Quota Alerts**

When spending reaches a fixed threshold of the quota, it notifies department owners.

**Budgets**

Set a spending limit for Azure. Budgets can be set for subscriptions, resource groups, service types,
etc. 

Budgets can send alerts, or suspend / modify resources after the trigger condition
