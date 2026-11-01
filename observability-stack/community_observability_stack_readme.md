# 🔭 Community Observability Stack

Welcome to the official, containerized observability stack built for developers, engineers, and tech communities! This repository provides a complete, out-of-the-box monitoring and telemetry environment using industry-standard tools: **Prometheus** (Metrics), **Loki** (Logs), **Tempo** (Traces), **Grafana** (Visualization), and **k6** (Load Testing).

## 🚀 Components Included

* **Grafana** (`http://localhost:3000`): The unified dashboarding and visualization layer.

* **Prometheus**: Metrics collection and time-series database.

* **Loki**: Log aggregation system designed for efficiency and scalability.

* **Tempo**: High-volume distributed tracing backend.

* **k6**: Developer-centric load testing and performance tool.

## 🛠️ Prerequisites

* [Docker Desktop](https://www.docker.com/products/docker-desktop/) installed and running on your machine.

* Git (if cloning the repository).

## ⚙️ Quick Start Commands

Follow these steps to initialize and run your observability stack:

### 1. Open Your Terminal

Navigate to your project folder where your `docker-compose.yml` is located:

```
cd observability-stack

```

### 2. Spin Up the Stack

Run the following Docker Compose command to start all services in detached mode:

```
docker compose up -d

```

> *Note: If you receive a warning about an obsolete `version` attribute in your `docker-compose.yml` file, it can safely be removed or ignored as modern Docker Compose versions handle it automatically.*

### 3. Verify Container Status

Check that all monitoring containers (`prometheus`, `loki`, `grafana`, `tempo`) are running successfully:

```
docker ps

```

### 4. Access Grafana Dashboard

Open your web browser and navigate to the local Grafana instance:
👉 [**http://localhost:3000**](http://localhost:3000)

## 📁 Project Directory Structure

```
observability-stack/
├── grafana/       # Grafana datasources, plugins, and custom dashboards
├── k6/            # Performance and load testing scripts
├── loki/          # Loki configuration files
├── prometheus/    # Prometheus target scrape configurations & rules
├── tempo/         # Tempo distributed tracing configurations
└── docker-compose.yml # Multi-container orchestration definition

```

## 🛑 Management & Shutdown Commands

* **Stop the services** (keeps data intact):

  ```
  docker compose stop
  
  ```

* **Tear down the stack** (removes containers and networks):

  ```
  docker compose down
  
  ```

* **Tear down and wipe persistent volumes** (Caution: clears all stored metrics/logs/traces data):

  ```
  docker compose down -v
  
  ```

## 💡 Community & Support

Built for the open-source and local developer community. Feel free to contribute custom dashboards, alerting rules, or sample application instrumentations to help others level up their DevOps and software engineering skills!