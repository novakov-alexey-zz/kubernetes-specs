## Kubernetes Istio Specs 

### Logging with Fluentd

Elasticsearch, Kibana, Fluentd specs based on Istio Official examples:

https://istio.io/docs/tasks/telemetry/fluentd/

There are few additions in these specs:

- ClusterRole, ServiceAccount
- Configuration for Fluentd kubernetes_metadata and in_tail_ plugin to grab Cluster logs into EFK stack

To apply these specs run:

```bash
kubectl apply -f logging-stack.yaml
kubectl apply -f fluentd-istio.yaml
``` 