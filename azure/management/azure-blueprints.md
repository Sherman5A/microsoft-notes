
# Azure Blueprints

Azure Blueprints,
> Allow for standardisation of deployments.

Configurations can follow a custom or pre-defined defined blueprint with policy settings pre-configured.

Blueprints are version-able, allowing for small updates.

## What are Artefacts?

> Each component defined in a blueprint is an **artefact**.

**Artefact Parameters:**

Artefacts can have additional parameters if required.

Parameters can be defined in the blueprint definition. They can also be assigned when the blueprint is applied to a
scope.

This means you maintain 1 standard blueprint, but have flexibility to specify relevant artefact
parameters.

Artefacts can include things like,
- Role assignments
- Policy assignments
- Azure resource manager templates
- Resource groups
