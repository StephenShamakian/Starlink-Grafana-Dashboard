# Starlink-Grafana-Dashboard
Grafana Dashboard for Starlink. Data is gathered using Sparky8512's Starlink GRPC Tools (Found here: https://github.com/sparky8512/starlink-grpc-tools). That utility imports metrics into InfluxDB at a determined interval (based on the paramenters used). This Grafana dashboard presents those metrics in a visual way. 

This dashboard was originally based off of Neurocis's Grafana Dashboard located here: https://github.com/sparky8512/starlink-grpc-tools/blob/main/GrafanaDashboard%20-%20Starlink%20Statistics.json

![Grafana-Starlink-Dashboard-Screenshot](https://user-images.githubusercontent.com/6382844/126184441-a308ba83-20e5-4ff1-812d-f1971c59971d.PNG)

## Requirements
- Sparky8512's Starlink GRPC Tools (https://github.com/sparky8512/starlink-grpc-tools) exporting metrics to InfluxDB
  - I run it in a container: https://github.com/sparky8512/starlink-grpc-tools#docker-for-influxdb---mqtt-under-development-
  - I use the dish_grpc_influx.py script with the following parameters: dish_grpc_influx.py -t 3 --all-samples --no-counter --numeric -v status obstruction_detail ping_drop ping_run_length ping_latency ping_loaded_latency usage alert_detail bulk_history
- Grafana v7.5 or higher
- Grafana Plugin: Pie Chart v2
- Grafana Plugin: Radar Graph
- Grafana Plugin: AJAX
