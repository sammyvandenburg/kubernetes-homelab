# Kubernetes Homelab

Production Enterprise Kubernetes homelab built with Talos Linux, FluxCD, Cilium, observability, and day 2 operations in mind.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## Why this exists

Most homelab Kubernetes setups focus on getting a cluster running.

This project was built to demonstrate something stronger: how to design, document, and operate a production-style Kubernetes platform using modern infrastructure practices. The goal is not just to run workloads at home, but to show the kind of engineering judgment companies want to see when hiring DevOps and platform engineers.

---

## What this project demonstrates

- Kubernetes platform design
- GitOps-based operations
- Immutable infrastructure with Talos Linux
- Infrastructure as Code and repeatability
- Observability and monitoring
- Security-aware configuration
- Documentation and architectural decision-making
- Production-style project structure

---

## Architecture

```mermaid
flowchart TD
    GitRepo[Git Repository] --> FluxCD[FluxCD]
    FluxCD --> Cluster[Kubernetes Cluster]
    Cluster --> Apps[Application Workloads]
    Cluster --> Observability[Prometheus and Grafana]
    Cluster --> Networking[Cilium]
    Cluster --> Storage[Persistent Storage]
