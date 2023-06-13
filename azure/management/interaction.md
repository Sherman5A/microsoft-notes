
# Interacting with Azure

THere are several methods of interacting with Azure,
- Azure Portal
- Azure Powershell
- Azure CLI

## Azure Portal

Web-based GUI to manage Azure.

> Provides a browser-based shell that allows management of azure resources.

## Azure Powershell

Shell that allows cmdlets to be run. The cmdlets allows people to call the REST API to perform
management.

## Azure CLI

Similar to Azure Powershell, however it uses Bash commands instead of Powershell.

# Azure Arc

Azure Arc
> Provides resource management and monitoring for both Azure and on-premises resources.

This provides:
- Centralised management of an organisations entire environment
- Management of on-prem resources as if they were running on Azure
- Ability to use familiar Azure capabilities

Azure arc can manage:
- Servers
- K8 clusters
- Azure data services
- SQL servers
- VMs

# Azure Resource Manager

Azure Rsource Manager (ARM),
> Allows you to create, update, and delete resources.

When a user sends a request through an interfaec, ARM recieves the request, then proceeds to authenticate
it. Then, ARM sends the request to the relevant service.

Azure resource manager allows,
- Manage infrastructure through templates made in JSON
- Deploy resources as a group, rather than individually
- Redeployment of solution
- Definition of dependencies
- Apply access control through ARM integration with RBAC
- Apply tags
- View costs

## ARM Templates

ARM templates provide infrastructure as code.

ARM templates allow you to describe resources you require in a JSON format. Resources specified in
ARM tempaltes are checked, and then deployed in parallel.

Benefits:
- Declarative
    - You write what you want, you do not write how to do it
- Repeatable Results
    - Deployments occur in a consistent manner
    - Same ARM template can be used several times, all instances will be the same
- Orchestration
    - No need to worry about ordering operations
    - ARM orchestrates order of resources to ensure correct creation order
    - Template is deployed through 1 command
- Modular Files
    - Templates can be broken into smaller, reusable components and then linked
- Extensibility
    - Ability to add PowerShell / Bash to templates

