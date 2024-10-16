
# K8s-Insight

This repo contains Kubernetes configs and Helm charts for deploying services like Elasticsearch, NGINX, Prometheus, and Grafana.

## Setup

1. **Create Cluster**:
   ```bash
   kind create cluster --config kind-config.yaml
   ```

2. **Deploy NGINX**:
   ```bash
   helm install my-nginx bitnami/nginx -f nginx-values.yaml
   ```

3. **Deploy Elasticsearch**:
   ```bash
   helm install elasticsearch elastic/elasticsearch -f elasticsearch-values.yaml
   ```

4. **Deploy Prometheus**:
   ```bash
   helm install prometheus prometheus-community/prometheus -f prometheus-values.yaml
   ```

5. **Deploy Grafana**:
   ```bash
   helm install grafana grafana/grafana -f grafana-values.yaml
   ```

## Access Grafana:
```bash
kubectl port-forward svc/grafana 3000:80
```
Then open `http://localhost:3000` in your browser.

## Tools:
- Docker
- Kubectl
- Kind
- Helm
