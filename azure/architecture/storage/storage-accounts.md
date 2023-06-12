
# Storage Accounts

Storage accounts offers several redundancy options:
- Locally redundant storage **(LRS)**
- Geo-redundant storage **(GRS)**
- Read-acess goe-redundant storage **(RA-GRS)**
- Zone-redundant storage **(ZRS)**
- Geo-zone-redundant storage **(GZRS)**
- Read-access geo-zone-redundant storage **(RA-GZRS)**

All storage devices have a unique namespace available to access.

## Storage Redundancy

Several copies of data are stored to ensure data redundancy.

Several redundancy options are offered depending on costs and availability.

### Primary Region Redundancy

#### Locally Redundant Storage **(LRS)**

[[locally-redundant-storage.png]]

LRS replicates the data 3 times within a single data center in the primary region.

> This provides 11 nines of durability over a year.

#### Zone Redundant Storage **(ZRS)**

[[zone-redundant-storage.png]]

Replicates data synchronously across 3 Azure availabilty zones in the primary region.

> This provides 12 nines of durability over a year.

If a zone becomes unavailable, no remounting is required and DNS automatically repoints.

### Secondary Region Redundancy 

For applications that require high durability and redundancy.

By default, data in the secondary region is not available to read or write unless the primary region
fails. Data loss can happen on changeover as data is not synced synchronously.

#### Geo-Redundant Storage **(GRS)**

[[geo-redundant-storage.png]]

Data copies 3 times in a single data center in the primary region using Locally Redundant Storage.
Data is copied asynchronously to a single data center in the secondary location using LRS.

> This provides at least 16 nines of durability over a year.

#### Geo-zone-redundant storage **(G

[[geo-zone-redundant-storage.png]]

Data copied synchronously across 3 availability zones in the primary region. It is then replicated 3
times in the secondary region to a single data center through LRS.

> This provides at least 16 nines of durability over a year.

## Storage Services

Storage services are accessible by HTTP, HTTPS, and with frameworks and programming libraries.
Furthermore, a REST API is offered.

### Azure Blobs

Storage for unstrucuted data such as images, text, video, and audio.

Can also take binary data strams.

3 Tiers:
- Hot
    - Optimised for frequently accessed data
- Cold
    - Data that is infrequently accessed and stored for at least 30 days
    - Lower availability
    - Higher access costs than hot data
    - Cheaper storage costs than hot data
- Archive - Data that is rarely accessed and stored for at least 180 days
    - Stores data offline
    - Lowest storage costs
    - Higest costs to rehydrate and retrieve data

### Azure Files

Offers online file systems.

Systems accessible by SMB or NFS protocols.

They can be mounted by cloud, or onto on-prem delpoyments at the same time.

Benefits:
- Familiar system - Using NFS and SMB allows developers to access using standard I/O calls.
- Shared access - Do not have to worry about compatability and integrity.

### Azure Queue Storage

Storing large numbers of messages.

Contain as many messages as possible, with each message up to 64kb in size.

> Commonly used to create a work backlog to process

Can be combined with Azure Functions.

### Azure Disk Storage

Volumes designed for use with VMs.

Both hard drives and SSDs available depending on storage requirements.

