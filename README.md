# 📈 Cloud Application Autoscaling & Monitoring System

A complete Cloud Computing (VCC) pipeline featuring a **Python Flask** web application, automated dynamic **Autoscaling Shell Scripts**, and real-time observability using **Prometheus** and **Grafana**.

This project monitors system performance metrics in real-time, visualizes telemetry data on custom Grafana dashboards, and triggers automated scaling actions based on metric thresholds.

---

## 🏗️ Architecture & Workflow

1. **Flask Web Application (`app.py`)**: Exposes web endpoints and exports application metrics.
2. **Prometheus (`prometheus.yml`)**: Scrapes and collects system performance metrics from the Flask application at configured intervals.
3. **Grafana (`grafana.ini`)**: Connects to Prometheus as a data source to visualize CPU, memory, and request throughput.
4. **Monitoring Script (`monitor.sh`)**: Continually checks application health and system metrics.
5. **Autoscaling Script (`autoscale.sh`)**: Dynamically provisions or de-provisions resources when CPU/memory thresholds are crossed.

---

## 📁 Repository Structure

```text
.
├── app.py              # Main Python Flask application with metrics export[cite: 9]
├── monitor.sh          # System resource & metric monitoring shell script[cite: 9]
├── autoscale.sh        # Threshold-based dynamic autoscaling script[cite: 9]
├── prometheus.yml      # Prometheus scraper and target metrics configuration[cite: 9]
├── grafana.ini         # Grafana dashboard & datasource server settings[cite: 9]
└── README.md           # Project documentation
