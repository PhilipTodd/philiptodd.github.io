---
layout: default
title: Projects
permalink: /projects/
---

# Projects

## Reference Projects

This page contains public reference projects demonstrating modern software engineering practices using .NET, Azure, distributed systems, DevOps, and infrastructure as code.

Each project is intended to show practical implementation, not just theoretical architecture.

---

## Azure Distributed Systems Reference

A production-style reference platform demonstrating cloud-native distributed systems on Microsoft Azure.

### Purpose

This project demonstrates how independently deployable services can be designed, integrated, secured, deployed, and monitored using Azure platform services.

### Key Concepts

- Microservices
- REST APIs
- Asynchronous messaging
- Database-per-service
- Cloud-native deployment
- Infrastructure as Code
- CI/CD pipelines
- Observability

### Technology Stack

- .NET 10 / C#
- ASP.NET Core
- Azure Container Apps
- Azure Service Bus
- Azure SQL
- Microsoft Entra ID
- Azure DevOps
- Bicep
- Application Insights
- Log Analytics

### Demonstrates

- Service decomposition
- API gateway / BFF pattern
- Secure service communication
- Azure-hosted workloads
- Automated infrastructure deployment
- Environment-specific configuration
- Monitoring and diagnostics

### Links

<!-- - **Source Code:** [github](https://github.com/philiptodd/azure-distributed-systems-reference) -->
- **Source Code:** [github](https://github.com/philiptodd/azure-distributed-systems-reference){:target="_blank"}
- **Architecture:** *Coming soon*
- **Live Demo:** *Coming soon*

---

## Event Sourcing Reference Platform

An event-sourced enterprise application reference project inspired by industrial planning and operational systems.

### Purpose

This project demonstrates how an application can use domain events as the system of record, with projections used to support query models, reporting, and operational views.

### Key Concepts

- Event Sourcing
- CQRS
- Domain-Driven Design
- Aggregate roots
- Immutable business events
- Asynchronous projections
- Read model synchronisation
- Message-based integration

### Technology Stack

- .NET 10 / C#
- ASP.NET Core
- Azure Cosmos DB
- Azure SQL
- Azure Service Bus
- Angular
- Microsoft Entra ID
- Azure App Service
- Azure DevOps
- Bicep
- Application Insights
- Log Analytics

### Demonstrates

- Cosmos DB event store
- Azure SQL read model projections
- Command/query separation
- Domain event modelling
- Projection rebuilding
- Asynchronous event publishing
- API design for event-sourced systems
- Cloud deployment using Azure PaaS

### Links

- **Source Code:** [github](https://github.com/philiptodd/blastiq-event-sourcing-reference){:target="_blank"}
- **Architecture:** *Coming soon*
- **Live Demo:** *Coming soon*

---

## Architecture Documentation

The reference projects include architecture documentation using C4 modelling and practical system design documentation.

### Documentation Includes

- System context diagrams
- Container diagrams
- Deployment diagrams
- Dynamic flow diagrams
- Architecture decision records
- Infrastructure notes
- CI/CD pipeline documentation

### Tools and Practices

- Structurizr DSL
- C4 Model
- Markdown documentation
- Architecture Decision Records
- Azure architecture diagrams

---

## Project Goals

These projects are designed to demonstrate the ability to:

- Design cloud-native systems.
- Build production-style .NET applications.
- Apply modern Azure platform services.
- Use event-driven and distributed architecture patterns.
- Automate infrastructure and deployment.
- Communicate architecture clearly.
- Balance technical design with business outcomes.

---

## Current Status

The projects are under active development.

As they mature, this page will be updated with:

- Architecture diagrams
- Screenshots
- Running Azure-hosted demonstrations
- CI/CD pipeline examples
- Deployment notes
- Observability examples

---

> These projects are public, practical demonstrations of software engineering capability across architecture, implementation, deployment, and operations.
