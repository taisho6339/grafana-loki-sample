## Install

1. Install minio

```bash
kubectl apply -f minio.yaml
```

2. Access to minio and create a bucket "grafana-loki"

3. Install Grafana Loki

```bash
helm upgrade --install local-loki grafana/loki-distributed -f loki-values.yaml
```

4. Install Promtail

```bash
helm upgrade --install local-promtail grafana/promtail -f promtail-values.yaml
```

5. Install grafana

```bash
kubectl apply -f grafana.yaml
```

6. Integrate with Loki on grafana