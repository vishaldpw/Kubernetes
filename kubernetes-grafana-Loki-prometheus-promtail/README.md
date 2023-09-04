Refer the Link Below
https://github.com/Cloud-Native-Security/monitor-security  

*************************************
We will be installaing only following
**************************
Prometheus Stack Helm Chart
Grafana
Promtail & Loki
******************************


We have to only run following commands

$kubectl create ns monitoring

$helm repo add prometheus-community https://prometheus-community.github.io/helm-charts

$helm upgrade --install prom prometheus-community/kube-prometheus-stack -n monitoring --values observability-conf/prom-values.yaml

$helm upgrade --install promtail grafana/promtail -f observability-conf/promtail-values.yaml -n monitoring

$helm upgrade --install loki grafana/loki-distributed -n monitoring

Do Not install tracee and trivy
