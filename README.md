# Installing Node Exporter and Centralized Prometheus Using Ansible

This guide provides an Ansible-based solution to install and configure Prometheus and Node Exporter on remote servers. It covers deploying Node Exporter for monitoring metrics like CPU, disk, and memory usage, and setting up a centralized Prometheus server to aggregate these metrics.

## Prerequisites

1. Ensure you have an inventory file listing the IP addresses of your remote servers.
2. Update the `ansible_user` in the inventory file to match the username for SSH access to your remote servers.

## Steps to Install and Configure

### 1. Install Node Exporter on Remote Nodes
Run the `Node_Exporter_Installing.yml` playbook on all nodes you want to monitor. This playbook sets up Node Exporter, which collects system metrics.

### 2. Set Up a Centralized Prometheus Server
Run the `Prometheus_Installing.yml` playbook to configure a central Prometheus server. This server will gather and display metrics from all monitored nodes.

### 3. Automatic Integration
The playbook automatically integrates the Node Exporter servers with the Prometheus server, ensuring seamless monitoring.

## Accessing Prometheus and Node Exporter

### Prometheus Web Interface
After installation, open your browser and navigate to:
```
<IP address of Prometheus server>:9090
```
Prometheus uses port `9090` by default.

### Verify Node Exporter Integration
To check if Node Exporter is successfully integrated with Prometheus, go to:
```
<IP address of Prometheus server>:9090/targets
```

### Access Node Exporter Metrics Directly
To view Node Exporter metrics for a specific node, navigate to:
```
<IP address of remote node>:9100
```
Node Exporter runs on port `9100` by default.

## Checklist ✅ 
- [x] Run `Node_Exporter_Installing.yml` on all monitoring nodes.
- [x] Run `Prometheus_Installing.yml` on the centralized Prometheus server.
- [x] Verify Prometheus and Node Exporter integration through the browser.

