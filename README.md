# Prometheus Monitoring for Containerized Applications
Monitor your Docker containers using prometheus, cAdvisor , node-exporter and grafana
## Prerequisites:
* [Docker CE](https://docs.docker.com/install/), Docker EE, or [Docker Desktop on Windows](https://docs.docker.com/docker-for-windows/install/)
* [docker-compose](https://docs.docker.com/compose/install/)

## Setup and Deploy the monitoring stack
1. Clone this repo:
    ```bash
    git clone https://github.com/jmb12686/prometheus-monitoring
    cd prometheus-monitoring
    ```

2. Change line #5 in the `alert.rules.yml ` file to correspond to a container name that you want to explicitly monitor and fire alerts for.  Change `name="YOUR-CONTAINER-NAME-HERE"` to match your Docker container NAME.

3. Start the stack with docker-compose:
    ```bash
    docker-compose up
    ```

    If launching from a Windows host, be sure to set the following Docker-Compose variable in powershell first:
    ```powershell
    $Env:COMPOSE_CONVERT_WINDOWS_PATHS=1
    ```

## Dashboards
Links to dashboards of each monitoring tool deployed in this stack
* **cAdvisor** - Collects and exports resource usage and performance statistics of Docker containers.
    * http://localhost:9200

* **node-exporter** - Prometheus exporter for hardware and OS metrics
    * http://localhost:9100

* **Prometheus** - Prometheus monitoring system and time series database. 
    * http://localhost:9090

* **Grafana** - monitoring, metric analytics, and dashboard visualization tool.
    * http://localhost:3000
    * default user/pass : admin/admin


