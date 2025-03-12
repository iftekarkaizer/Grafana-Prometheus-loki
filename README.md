Summary of What Has Been Done

Loki Setup (Port 4100)

Configured loki (loki-local-config.yaml).
Installed and configured Loki to collect logs.
Changed the port to 4100 before running Loki.
Verified logs through the browser at http://<your-server-ip>:4100/metrics.

Grafana Setup (Port 4200)

Installed Grafana from the official repository.
Changed Grafana’s port to 4200.
Restarted the Grafana service and verified it via http://<your-server-ip>:4200.
Configured log filtering using {job="promtail"} |= "error" for error logs.
Prometheus Setup (Port 9090)

Installed and configured Prometheus.
Created a system service for Prometheus.
Set up configuration files to scrape data from various sources.
Verified Prometheus at http://<your-server-ip>:9090.
Promtail Setup (Log Collection from /var/log)

Installed Promtail to forward logs to Loki.
Configured promtail-config.yaml to scrape logs from /var/log/syslog.
Created a Promtail service to start it automatically.
Verified log forwarding to Loki.
Node Exporter Setup (CPU, RAM Monitoring)

Installed node_exporter to collect system metrics.
Configured Prometheus to scrape node metrics from 192.168.1.227:9100 and 192.168.1.246:9100.
Verified node metrics via http://<your-node-ip>:9100.
Grafana Dashboards

Imported Dashboard 1860 for CPU, RAM metrics.
Imported Dashboard 13639 for Log monitoring with Loki.

What Can Be Achieved?


✅ Centralized Log Management → Logs from multiple sources (system logs, applications) are collected and visualized in Grafana.
✅ Real-time System Monitoring → CPU, RAM, and other system metrics are monitored via Prometheus and Node Exporter.
✅ Alerting & Filtering → Prometheus and Grafana allow custom alerts based on logs and metrics.
✅ Scalability → Can be extended to monitor multiple machines, applications, and cloud instances.
