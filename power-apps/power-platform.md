
# Microsoft Power Platform

![[power-platform.png]]

Microsoft Power Platform:

> Low-code platform for building business apps quickly.

4 main components:
- Power Apps
- Power Automate
- Power BI
- Power Virtual Agents

Components can be used individually, or together.

The platform uses a low-code amount approach, allowing everyone to help build apps.

Developers can leverage integration with Azure to extend Power Platform.

## Power Apps Applications

Apps created with Power Apps are consumed using desktop or mobile devices.

Power Apps have 3 types:
- **Canvas**
    - Provide maker with precise control over screen contents and navigation
    - Use connectors to work with data and services
    - Can be embedded into SharePoint, Teams, Power BI, Dynamics 365
- **Model-driven**
    - Data-driven applications built on Microsoft Dataverse
    - Other sources and services can be used by model-driven applications by embedding canvas
      applications
- **Portal / Power pages**
    - Create external websites.
    - Outsiders can sign into website and view data

Key developer extensibility points of Power Apps:
- Building custom visual controls with **Power Apps Component Framework** *(PCF)*
- Implementing client logic with JavaScript and APIs
- Building custom connectors for external data sources through Azure services
- Building HTML web resources

## Power Apps Components

### Power Automate

Power Automate:
> Automate tasks and orchestrate activities using connectors

Power Automate can create:
- **Cloud Flows**
    - Triggered manually or when certain events happen
    - Built on Azure Logic Apps
- **Desktop Flows**
    - Automate repetitive tasks on web or desktop

Key developer extensibility points of Power Apps:
- Building custom connectors with Azure services
- Use workflow functions to build complex expressions

### Power BI

Power BI:
> Business analytics tool that provides data visualisation. Helps users visualise and share data across
> organisation

Key developer extensibility points of Power Apps:
- Embed Power BI in apps, websites, portals
- Create custom data visuals
- Use Power BI's API to run automatic processes, scaling, and management
- Develop Power Query connectors to access data from external data sources

### Power Virutal Agents

Power Virtual Agents:
> Create powerful chatbots that answer questions from customers, employees, etc.

Key developer extensibility points of Power Apps:
- Build bot framework skills
- Extend bots with Bot Framework Composer

## Connectors

Connector:
> Proxy / wrapper around an API that allows a service to communicate with Power Automate, Power Apps,
> and AAzure Logic Apps

This is a key component in accessing data and services. It provides a way for users to connect their
accounts nad use actions to build apps and workflows.

Many pre-built connectors are available for use. Custom connectors can be made for APIs.

## Dataverse

Dataverse:
> Cloud scale data store that abstracts data management from developer.

Dataverse stores data in data tables, and access is controlled by RBAC.

Dataverse can be extended by adding custom logic. Table columns, rules workflows, and process flows can
be customised to ensure business procedures are followed.

Key developer extensibility points of Power Apps:
- Create plug-ins that customise data processing in Dataverse with custom logic
- Use webhooks and Azure to integrate with external systems
- Extend Dataverse's API with your own custom API
- Use virtual tables to integrate extrenal systems with Dataverse without replication

### Common Data Model

Open-source standard definition of entities that represent common concepts and activities.

Dataverse includes a core set of entities that can be expanded on with custom entities.

