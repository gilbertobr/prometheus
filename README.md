# LEIA-ME

## Prometheus
 * docker pull prom/prometheus
 * docker run --name prometheus -p 9090:9090 -p 9093:9093 -p 9094:9094 -v /root/Prometheus/prometheus.yml:/etc/prometheus/prometheus.yml -v /root/Prometheus/rules:/etc/prometheus/rules -v /root/Prometheus/alertmanager:/etc/alertmanager -v /root/Prometheus/alertmanager/alertmanager:/usr/local/bin/alertmanager -d prom/prometheus

## Alertmanager

 * curl -LO https://github.com/prometheus/alertmanager/releases/download/v0.18.0/alertmanager-0.18.0.linux-amd64.tar.gz (Fora Docker)
 * mkdir -p /var/lib/alertmanager/data (Docker)
 * chmod +x /usr/local/bin/alertmanager (Docker)
 * chmod +x /etc/systemd/system/alertmanager.service (Docker)
 * nohup /usr/local/bin/alertmanager --config.file=/etc/alertmanager/config-rc.yml --storage.path /var/lib/alertmanager/data & (Docker)
