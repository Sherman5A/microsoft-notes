
# Azure Policy

Azure policies,
> Tool that allows you to create policies that control resources. Enforce rules across configurations to 
> keep compliance with standards.

Both individual and group related policies. These are called **initiatives**.

Resources that do not comply with created policies are highlighted.

Policies can be set at each level of Azure management. This means, resources, resource groups,
subscriptions, etc. Moreover, Azure policies are inherited.

Azure policies are capable of fixing erroneous resource configurations for resources to keep integrity.

# Policy Initiatives

Policy initiatives,
> Grouping related policies together.

**Example:** *Enable Monitoring in Azure Security Centre*

This policy initiative includes:
- Monitor unencrypted SQL Databases
- Monitor OS vulnerabilities
- Monitor missing Endpoint Protection

