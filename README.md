## Install

```
kubectl apply -f minio.yaml
kubectl apply -f grafana.yaml

helm upgrade --install local-loki grafana/loki-distributed -f loki-values.yaml
helm upgrade --install local-promtail grafana/promtail -f promtail-values.yaml
```
