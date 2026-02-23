
Local observability setup using Prometheus, OpenTelemetry and Grafana
📊 Local Observability Stack
This project demonstrates a local monitoring setup using:
Prometheus for metrics scraping
OpenTelemetry Collector for telemetry processing
Grafana for visualization
System metrics exposed via /metrics endpoint

🏗 Architecture
Application → Prometheus → Grafana
Prometheus scrapes metrics from localhost and stores time-series data, which is visualized in Grafana dashboards.

📈 Metrics Monitored
system_cpu_time_seconds_total
disk operations
filesystem usage
network packets
scrape duration

🚀 How to Run
Start application exposing /metrics
Start Prometheus
Start Grafana

Access:
Prometheus: http://localhost:9090
Grafana: http://localhost:3000

On prometheus:
Verify: Go to http://localhost:9090/targets. You should see pc-health with a Green "UP" status.

visualization steps in grafana:
Connect your Data Source
Before building graphs, ensure Grafana is talking to Prometheus.
Open Grafana (http://localhost:3000).
Go to Connections > Data Sources.
Click Add data source and select Prometheus.
In the URL field, type: http://prometheus:9090.
Note: Use the
service name "prometheus" because they are in the same Docker network.
Scroll to the bottom and click Save & Test. You should see a green "Data source is working" message.
<img width="960" height="540" alt="Screenshot 2026-02-23 091410" src="https://github.com/user-attachments/assets/02903196-a633-4e62-a2c6-3bc4003ca319" />
<img width="950" height="424" alt="Screenshot 2026-02-23 094529" src="https://github.com/user-attachments/assets/cecf9107-7ae2-4ee1-ac18-d8b13fafe8e3" />


