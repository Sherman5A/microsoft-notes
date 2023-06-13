
# VPN Gateways

VPN gateways enable,
- Connecting on-premises datacenters to virtual networks **(site-to-site)**
- Connecting devices to virtual networks **(point-to-site)**
- Connecting virtual works to other virtual networks **(network-to-network)**

Two types of VPNs:

1. Policy-based
    - Specify **statically** IP address of packets through each tunnel.
    - Every data packet is evaluating against a set of IP addresses to choose the tunnel where the
      packet is sent.
2. Route-based
    - IPSec tunnels modelled as network interfaces. IP routing then decides which tunnel interfaces to use
      for each packet.
    - This makes route-based VPNs more resilient to changes in network topology.

Route-based gateways are used when you require:
- Connections between virtual networks
- Point to site connections
- Multi-site connections

# VPN Availability

VPNs must be highly available and fault tolerant.

## Active / Standby

VPNs are deployed as 2 instances in a active, standby configuration.

> When the active instance is disturbed, the standby instance takes over.

Connections are interrupted, but they are restored quickly.

## Active / Active

Each VPN instance has its own public IP. Separate tunnels are created from the on-premises devices to
each public IP. This increases reliability.

## ExpressRoute Fail-over

If ExpressRoute fails, VPN gateways can be used as an alternative.

## Zone-Redundant Gateways

Protects from zone-level failures.
