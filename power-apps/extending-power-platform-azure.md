
# Extending Power Platform with Azure

## Azure Functions

![[azure-function.png]]

Azure Function offload logic from the Power application, improving stability and user experience.

## API Management

Azure API management allows you to manage on-premises and cloud APIs.

APIs can be expoerted directly to Microsoft Power Platform. When exported the API is configured as a
custom connector.

## Service Bus

Service Bus:
> Messaging-as-a-service *(MaaS)* framework that enables real-time, asynchronous messaging accross
systems.

This can integrate cloud and on-premises systems in serverless distributed fashion.

Due to the asynchronous nature, the bus can store the message until the recieving party is ready to
recieve the messages.

## Event Grid

Event Grid:
> Service for managing reouting of events from a source to a destination.

This simplifies event-based applications. Events Grid can be used to route events between Power Platform
and Azure Services.

## Logic Apps

Logic Apps:
> Cloud service that schedules, automates, and orchestrate tasks, processes, and workflows.

Power Automate is similar to Logic Apps. However, it is used when automation needs support unavailable
in Power Automate. Logic Apps offers a different deployment and consumption model that is better
in certain scenarios.

## Cognitive Services

Family of AI and APIs that help with app creation. Power Platform offers AI Builder service, which is
a low code option for AI APIs.

When the requirements become too complex, Cognitive Services are required.

Cognitive Services offers APIs, SDKs, and services that help developers add cognitive features.

5 main pillars:
- Speech
- Vision
- Language
- Web search
- Decision

## Azure Bot Service

Framework to create intelligent bots. Azure Bot Framework Skills can be integrated with Power Virtual
Agents to add custom code processing to Power Virutal Agents.

## Azure Data Lake & Azure Synapse Analytics

Azure Data Lake Storage:
> Large scalable storage for data anaylsis.

Azure Synapse Link:
> Near real-time data analysis

Data and metadata changes in Dataverse are automatically pushed to Azure Synapse and Azure Data Link

## Azure SQL Database

Dataverse is built on Azure SQL Database engine. SQL connection is provides allow for read-only access
of Dataverse environments.

## Other Services

- App Service
- Identity Management
- Interent of Things
- DevOps
- Developer Tools

