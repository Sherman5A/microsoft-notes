
# Azure Virutal Networking

> Allow Azure resources to communicate with each other, the internet and on-prem devices.
\
> Extension of on-prem network with linked Azure resources.

Provides:
- Isolation
- Internet communcication
- Azure resource communcication
- On-prem communcication
- Route network traffic
- Filter network traffic
- Connect virtual networks

Azure virtual networks can have public and private access endpoints

## Isolation & Segmentation

Multiple isolated networks can be created.

Pirvate IP ranges are created and only exist within the network. These ranges can be further divided
with subnets.

Azure offers DNS for virutal networks.

## Internet Communications

Resources can be assigned a public IP or be placed in a public load balancer to enable public
connections.

## Azure Resource Communications

- Virtual networks can be used to connect Azure resources.
- Service endpoints can connect to other Azure resource types. An Azure SQL database can connect to
  storage accounts.

## On-Prem Communication

Create a network spanning local and cloud environments

- Point-to-site virtual private network
    - Connection from computer outside network to corporate network
    - Using a VPN connection to connect to Azure virtual network
- Site-to-site virtual private network
    - Links a on-prem VPN to Azure VPN gateway in the virtual network
    - Azure appears to be part of the local network
- Azure ExpressRoute
    - Dedicated private connectivity to Azure, not over the internet
    - Designed for high bandwidth and high security

## Network Traffic Routing

Azure routes everything by default.
- Azure allow for custom routing tables
- Border Gateway Protocol on VPN gateways

## Filter Network Traffic

Allows for traffic filtering between subnets
- Network Security groups allow for inbound and outbound security rules
- Network virtual appliances are specialised VMs that run firewalls or WAN optimisation

## Connect Virutal Networks

Virtual networks linked through virtual network peering, allowing multiple networks to connect 
directly to each other.

- Traffic is private
- Does not enter public interent
- Networks can be in seperate regions
