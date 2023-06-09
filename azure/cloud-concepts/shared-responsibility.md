
# Introduction to Cloud Computing

Cloud computing allows for:
- Computer's performance and specifications can be changed to suit situation.
    - Easier to scale with the growth of the business. 

## Shared Responsibility Model

**Traditional Corporate Datacenter:**

> Company must maintain physical space, replace hardware, maintain infrastructre and software.
> Keep software updated and secure.

**Shared Responsibility Model:**

> Shared between cloud provider and consumer.

Cloud manages:
- Physical security
- Power
- Hardware
- Cooling
- etc.

Consumer responsbile for:
- Data stored in providers data center.
- Access security.
- Data ingest

If you yourself deploy a VM and install an SQL database, you would then manage
the database software and contents.


There can be varying levels of responsibilities.

These rank from having most responsbility on the consumer to the least responsbility on the consumer:
- Infrastrucutre as a Service (IaaS)
- Platform as a service (PaaS)
- Software as a service (SaaS)

![[shared-responsbility.svg]]

No matter the level,

Consumers are responsbile for:
- Info stored on cloud
- Access
- Accounts

Providers are responsbile for:
- Hardware
- Network
- Hosting

Responsibility varies with:
- OS
- Software
- Infrastructure
- Network controls

