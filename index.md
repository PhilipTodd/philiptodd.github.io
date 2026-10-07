---
layout: default
title: Philip Todd | Cloud Architect & Senior .NET Engineer
---

<section class="hero">
  <div class="content-container">
    <div class="hero-pill">ENTERPRISE .NET 10 & AZURE CLOUD ARCHITECTURE</div>
    <h1>Philip Todd</h1>
    <p class="hero-tagline">
      Senior software engineer - Technical leader. 25+ years designing, implementing, and deploying enterprise-grade distributed systems on Microsoft Azure.
    </p>
    <div class="hero-buttons">
      <a href="#projects" class="btn btn-primary">Inspect Reference Platforms</a>
      <a href="#architecture" class="btn btn-secondary">Explore C4 Models</a>
      <a href="{{ '/resume/' | relative_url }}" class="btn btn-secondary">Career History</a>
    </div>
  </div>
</section>

<section id="projects" class="section">
  <div class="content-container">
    <h2 class="section-title">Reference Implementations</h2>
    <p class="section-subtitle">
    Working production-style systems deployed with automated CI/CD and Infrastructure as Code.</p>
    <div class="grid-3">
      {% for project in site.data.projects %}
      <div class="card">
        <div class="card-header">
          <h3 class="card-title">{{ project.title }}</h3>
          <span class="card-badge">{{ project.badge }}</span>
        </div>
        <p class="card-desc">{{ project.summary }}</p>
        <div class="tag-cloud">
          {% for t in project.tech %}
          <span class="tag-item">{{ t }}</span>
          {% endfor %}
        </div>
        <div class="metric-strip">
          {% for m in project.metrics %}
          <div class="metric-row">
            <span class="metric-label">{{ m.label }}:</span>
            <span class="metric-val">{{ m.value }}</span>
          </div>
          {% endfor %}
        </div>
        <div class="card-actions">
          {% if project.links.demo %}
          <a href="{{ project.links.demo }}" target="_blank">Live Demo ↗</a>
          {% endif %}
          <a href="{{ project.links.docs }}" target="_blank">Technical Docs ↗</a>
          <a href="{{ project.links.github }}" target="_blank">Source Code ↗</a>
        </div>
      </div>
      {% endfor %}
    </div>
  </div>  
</section>

<section id="architecture" class="section section-alt">
  <div class="content-container">
    <h2 class="section-title">C4 System Architecture & Topologies</h2>
    <p class="section-subtitle">System boundary, container, and asynchronous data-flow models generated via Structurizr DSL.</p>

    <div class="tab-nav">
      <button class="tab-btn active" onclick="showTab(event, 'c4-microservices')">Distributed Microservices (Parameter Pilot)</button>
      <button class="tab-btn" onclick="showTab(event, 'c4-event-sourcing')">Event Sourcing (Blast Planning)</button>
      <button class="tab-btn" onclick="showTab(event, 'c4-ticketing')">Ticketing System</button>
    </div>

    <div id="c4-microservices" class="tab-content">
      {% include c4-diagram.html
        id="distributed-system-c4"
        title="C4 Level 2: Container Diagram — Cloud-Native Distributed Microservices"
        summary="YARP Gateway → Container Apps (.NET 10 Microservices) → Azure Service Bus Pub/Sub → OpenTelemetry Correlation"
      %}
    </div>

    <div id="c4-event-sourcing" class="tab-content active">
      {% include c4-diagram.html
        id="event-sourcing-c4"
        title="C4 Level 2: Container Diagram — Event Sourced Blast Planning"
        summary="Angular UI → ASP.NET Core API → Cosmos DB (/streamId) → Service Bus Topic → Azure Function Worker → Azure SQL (Read Model)"
      %}
    </div>

    <div id="c4-ticketing" class="tab-content">
      {% include c4-diagram.html
        id="ticketing-c4"
        title="C4 Level 2: Container Diagram — Ticketing Reference Application"
        summary="Angular SPA → ASP.NET Core API → Azure SQL (ticketing schema) → Application Insights / Log Analytics"
      %}
    </div>
  </div>
</section>

<section class="section">
  <div class="content-container">
    <h2 class="section-title">Technical Expertise Taxonomy</h2>
    <p class="section-subtitle">Core capabilities across cloud systems, enterprise databases, and modern software engineering.</p>

    <div class="skills-grid">
      {% for group in site.data.skills %}
      <div class="skill-category">
        <h4>{{ group.category }}</h4>
        <ul class="skill-list">
          {% for item in group.items %}
          <li>{{ item }}</li>
          {% endfor %}
        </ul>
      </div>
      {% endfor %}
    </div>
  </div>
</section>

