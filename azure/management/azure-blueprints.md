
# Azure Blueprints

Allows standardisation of deployments.

Configurations can follow a defined blueprint with policy settings pre-configured.

## What are Artifacts?

Each component defined in a blueprint is an artifact.

Artifacts can have additional parameters if required.

Parameters can be defined by definition, or they can be assigned when the bluepront is applied to a
scope.

This means you maintain 1 standard blueprint, but have flexiblity to specify relevant artifact
parameters.

Artifacts can include things like,
- Role assignments
- Policy assignments
- Azure resource manager templates
- Resource groups

Blueprints are version-able, allowing for small updates.

