# Grafana Alloy

Learn how to collect different types of data using **Grafana Alloy components**. This repository contains resources and guides to help you get started with collecting logs, metrics, and traces using Alloy's observability tools.

## YouTube Playlist

This repository is associated with our Grafana Alloy YouTube playlist that covers the following topics:

### 1. Collecting Logs
- [Watch now: Collecting Logs](https://www.youtube.com/watch?v=tMSZ_DVq5pw)
  - Learn how to collect logs from various sources:
    - **Local files**: Collect logs from file-based sources.
    - **Systemd-journal**: Capture logs from systemd services.
    - **Docker containers**: Stream logs from Docker container logs.
    - **Kubernetes pods**: Gather logs from running Kubernetes pods.
  - All logs are sent to **Grafana Loki** via **Grafana Alloy**

### 2. Collecting Metrics
- **Coming Soon**  

### 3. Collecting Traces
- **Coming Soon**


## Sections

The following sections cover various **Alloy components** and how they can be utilized for logs, metrics, and traces:

- [Logs with Alloy](#1-logs-with-alloy)
- [Metrics with Alloy](#2-metrics-with-alloy)
- [Traces with Alloy](#3-traces-with-alloy)

### 1. Logs with Alloy
In this section, we explore various ways to collect logs from different sources into Loki, focusing on the following types of logs:

#### Local Files Logs
Local files contain logs from different applications and systems stored on the disk. These logs can include application logs, system logs, or any other custom logs written to files. We will show how to collect these types of logs.

- `local.file_match`: A component for identifying the local log files you want to monitor.
- `loki.source.file`: The source component that reads the log files.
- `loki.write`: Writes the logs from local files into Loki.

#### Systemd Journal Logs
Systemd is a system and service manager used by Linux distributions. Systemd logs contain messages about services, system events, and kernel logs. We will focus on collecting logs from the systemd journal.

- `loki.relabel`: A component to modify or filter the log labels before storing them.
- `loki.source.journal`: Collects logs from the systemd journal.
- `loki.write`: Writes the collected systemd journal logs into Loki.

#### Docker Container Logs
Docker containers generate logs related to containerized applications. These logs can include stdout, stderr, and application logs. We'll cover how to collect logs from Docker containers.

- `discovery.docker`: Discovers the running Docker containers.
- `discovery.relabel`: Used to relabel the discovered container logs.
- `loki.source.docker`: Collects logs from Docker containers.
- `loki.write`: Writes the container logs into Loki.

#### Kubernetes Pod Logs
Kubernetes pods generate logs from the containers running inside them. These logs include application logs, errors, and system-level logs. We will cover how to collect logs from Kubernetes pods.

- `discovery.kubernetes`: Discovers the Kubernetes pods running in the cluster.
- `discovery.relabel`: Relabels the pod logs based on specific rules.
- `local.file_match`: Matches local files to collect logs from containers running within the pods.
- `loki.source.file`: Collects logs from local files inside the pods.
- `loki.process`: Processes the pod logs before writing them to Loki.
- `loki.write`: Writes the Kubernetes pod logs into Loki.

For all related codes and configurations, [click here](./collecting-logs-with-alloy).

---

### 2. Metrics with Alloy
🚧 **Coming Soon:** This section will cover how to collect and analyze metrics using Alloy, one of its key components. Stay tuned for updates!

---

### 3. Traces with Alloy
🚧 **Coming Soon:** This section will provide a detailed guide on collecting and visualizing traces using Alloy. Stay tuned for updates!
