
# Cloud Service Types

![[shared-responsibility.svg]]

## Infrastructure as a Service *(IaaS)*

> Most flexible. Provides consumer with maximum amount of control for resources.

Cloud provider responsibilities:
- Hardware
- Network connectivity
- Physical security

Consumer responsibilities:
- Operating system, configuration
- Network configuration
- Database configuration
- Storage configuration
- etc.

> You are renting the hardware in a datacentre.

IaaS scenarios:
- Lift-and-shift migration: Migrating on-premises resources onto cloud services.
- Testing and development: Existing configurations for development and test environments that you
  must rapidly replicate. Environments can be manged quickly, maintaining complete control.

## Platform as a Service *(PaaS)*

> Middle ground of responsibility.

Cloud maintainer responsibilities:
- Hardware
- Network connectivity
- Physical security
- Operating systems
- Middleware
- Development tools
- Business tools

Consumer responsibilities:
- Data
- Devices
- Accounts

PaaS scenarios:
- Development frameworks: Create applications using framework components using features like scalability,
  high-availability, etc. This reduces the developers work
- Analytics: Organisations can analyse their data.

## Software as a Service *(SaaS)*

> Least felixible service model

Renting a fully developed infrastructure and application.

Cloud maintainer responsibilities:
- Everything except
    - Data input
    - Devices that connect to system
    - Users that access system

SaaS scenarios:
- Email
- Finance tracking
- Business applications

