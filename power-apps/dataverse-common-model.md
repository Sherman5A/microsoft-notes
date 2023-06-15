
# Microsoft Dataverse

Dataverse allows for secure storage and managment of data used by businesses.

- Data is stored in a set of tables.
- Table are  a set of rows *(records)* and columns *(fields / attributes)*

Power Apps use Dataverse tables to build applications.

**Dataverse Benefits:**

- Created with Azure SQL, Azure Storage, Cosmos DB
- Technologies are absracted
- Cloud-hosted makes it easy to manage
- Built in RBAC control to tables
- Several existing first-party apps

Dataverse works with:
- Relational data
- Non-relational
- Files
- Images
- Search data
- Data lake

All in one unified API.

Moreover, it inegrates with Power Apps, allowing for quick, scaleable application creation.

## Security Model

Dataverse provides role-based security to manage access control and priveleges. These privileges can
be applied at the table, or column level for granular control.

Furthermore, Dataverse provides hierarchies

- Manager hierarchy
    - Manager must be in same business department as the repot
- Position hierarchy
    -    Allows data access across departments

## Extensibility

Code-based customisation is refered to as extending an application.

Falls into two sets

### Extending User Experience

Power Apps Component Framework is used to create components used across all types of Power Apps

Model-driven Power Apps expose a JavaScript API that allows interaction and logic.

Power Pages use Liquid templating language and JavaScript to extend web pages.

Canvas apps do not offer scripting. However, they offer Microsoft Power Fx. Power Fx is a functional,
general-purpose, strong-typed language to create apps.

TypeScript is recommended to use in scripting scenarios.

### Extending Dataverse

When Dataverse does not support a feature. It can be extended with server-side plugin code.

Power Automate attempts to add this, however, it can not to everything plugins offer, especially in 
synchronous behaviour.

## Dataverse Solutions

Dataverse Solutions:
> Containers for apps and other components.

Solutions are used to transport apps and components to different environments. Microsoft packages first
party apps as solutions.

Solutions implement application lifecycle management in Power Platform by distrubting components across
environments.

> Application lifecycle management is the governance, development, and maintenance of programs.

# Common Data Model

Common data model:
> Extensible collection of schemas that represent common concepts. Allow for data and information
> exchange between different applications and data sources.

Common schemas simplify data considerably.

