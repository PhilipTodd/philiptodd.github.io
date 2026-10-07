---
layout: page
title: Technical Reference Projects
description: In-depth breakdowns, live links, and source repositories for reference platforms.
permalink: /projects/
---

The projects below are designed to demonstrate complete software delivery lifecycles: from domain modelling and C4 architecture to automated Bicep deployments, CI/CD, and live production endpoints.

## 1. Distributed Systems Reference Platform

Models cloud-native microservices communicating via decoupled asynchronous messaging boundaries on Microsoft Azure.

* **Key Concepts:** Containerised services, API Gateway/BFF patterns, resilient message handling, and distributed tracing.
* **Observability:** Centralised telemetry correlation across Service Bus boundaries using Application Insights and Log Analytics.
* **Architecture as Code:** Visualised using Structurizr DSL and C4 Model container diagrams.

{% include c4-diagram.html
  id="distributed-system-c4"
  title="C4 container diagram — distributed microservices on Azure"
%}

<div class="cta-group">
  <a href="https://parameterpilot.com" target="_blank" class="btn btn-primary">Launch Live Demo ↗</a>
  <a href="https://distributed-systems.ausdatatech.com.au" target="_blank" class="btn btn-primary">Architecture Documentation ↗</a>
  <a href="https://github.com/philiptodd/azure-distributed-systems-reference" target="_blank" class="btn btn-secondary">Source Code ↗</a>
</div>

## 2. Event Sourcing Reference Platform

Demonstrates an enterprise-scale, event-sourced system modeled around mining blast-planning workflows. It replaces traditional CRUD updates with immutable domain events, supporting auditability, historical state reconstruction, and independently scalable read models.

* **Architecture:** Command Query Responsibility Segregation (CQRS), Domain-Driven Design (DDD), Event Sourcing
* **Write Pipeline:** ASP.NET Core API validates commands and appends events into Azure Cosmos DB (`/streamId` partition) with optimistic concurrency.
* **Read Pipeline:** Committed events are published to Azure Service Bus Topics, where Azure Functions project denormalised views into Azure SQL Database.
* **Delivery & IaC:** Bicep templates deployed via Azure DevOps multi-stage pipelines with What-If validation.

{% include c4-diagram.html
  id="event-sourcing-c4"
  title="C4 container diagram — event sourced blast planning"
%}

<div class="cta-group">
  <a href="https://demo.event-sourcing.ausdatatech.com.au" target="_blank" class="btn btn-primary">Launch Live Demo ↗</a>
  <a href="https://event-sourcing.ausdatatech.com.au" target="_blank" class="btn btn-secondary">Documentation & ADRs ↗</a>
  <a href="https://github.com/philiptodd/mining-event-sourcing-reference" target="_blank" class="btn btn-secondary">Source Code ↗</a>
</div>

## 3. Ticketing Reference Application

Demonstrates pragmatic, production-ready full-stack software delivery without unnecessary architectural overhead.

* **Key Capabilities:** Dynamic filtering, sorting, pagination, and optimistic concurrency handling.
* **Database Design:** Isolated within the `ticketing` schema of a shared database with independent EF Core migration histories.
* **Testing:** HTTP boundary integration testing using `WebApplicationFactory` and in-memory SQLite.

{% include c4-diagram.html
  id="ticketing-c4"
  title="C4 container diagram — ticketing reference application"
%}

<div class="cta-group">
  <a href="https://demo.ticketing.ausdatatech.com.au" target="_blank" class="btn btn-primary">Launch Live Demo ↗</a>
  <a href="https://ticketing.ausdatatech.com.au" target="_blank" class="btn btn-secondary">Documentation & Decisions ↗</a>
  <a href="https://github.com/philiptodd/TicketTest" target="_blank" class="btn btn-secondary">Source Code ↗</a>
</div>
