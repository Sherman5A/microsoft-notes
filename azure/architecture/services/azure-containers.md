
# Azure Containers

VMs are limited to a single and configuration OS per VM.

> Running several runtime environments would require several VMs with several operating systems.

To run multiple instances of an application on a single host, we will use containers.

## What are Containers

Containers are a virtualisation environment, like VMs.

Multiple containers can be run on a single or virtual host.

However, in containers you don't manage the operating system for the container.

> VMs are an instance of OS


> Containers are lightweight and designed to be created, scaled, and stopped frequently.

Container Benefits:
- Lighter weight
- More agile
- Respond to changes on demand
- Quick restarts

> Most popular container engine is **docker**

## Container Explanation

Container bundles a program and its dependencies into one. This is called containerisation.

The bundle can be deployed to a container host.

A container host provides a standard runtime environment, abstracting the OS and infrastructure.

This makes it very simple to have several containers working together.

> Virtual machines virtualise hardware
/
> Containers virtualise OS

This simplifies development as the development environment can behave exactly like the runtime
environment.

## Container vs VM

If complete control of a runtime environment is required, a VM may be more suitable.

However, if easy scalability and portability is important, a containerised solution may be better.

## Container Usage Examples

Containers are commonly used in micro-service architectures,
- Break solution into small, independent pieces.
- Isolating pieces means easier maintenance, scaling, and updating.

