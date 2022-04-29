FROM grafana/grafana

COPY dashboards.yml /etc/grafana/provisioning/dashboards/dashboards.yml
COPY datasources.yml /etc/grafana/provisioning/datasources/datasources.yml
COPY node-exporter-full.json /etc/grafana/provisioning/dashboards/default.json

EXPOSE 3000
