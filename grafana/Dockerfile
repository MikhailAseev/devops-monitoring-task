FROM grafana/grafana-enterprise
COPY default.yml /etc/grafana/provisioning/datasources/default.yml
COPY node-exporter.yml /etc/grafana/provisioning/dashboards/default.yml
ADD dashboards /var/lib/grafana/dashboards
