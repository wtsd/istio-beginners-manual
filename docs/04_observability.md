# Observability

Istio integrates with telemetry tools to monitor applications.

Read more: https://istio.io/latest/docs/concepts/observability/


- **Metrics**. Istio generates a set of service metrics based on the four “golden signals” of monitoring (latency, traffic, errors, and saturation). Istio also provides detailed metrics for the mesh control plane. A default set of mesh monitoring dashboards built on top of these metrics is also provided.
- **Distributed Traces**. Istio generates distributed trace spans for each service, providing operators with a detailed understanding of call flows and service dependencies within a mesh.
- **Access Logs**. As traffic flows into a service within a mesh, Istio can generate a full record of each request, including source and destination metadata. This information enables operators to audit service behavior down to the individual workload instance level.


### Metrics
Istio exports metrics to **Prometheus**.


```bash
kubectl -n istio-system port-forward svc/prometheus 9090:9090
```


### Tracing
**Jaeger** or **Zipkin** can be used for distributed tracing.


```bash
kubectl -n istio-system port-forward svc/jaeger-query 16686:16686
```


### Kiali
Provides a graphical dashboard for service mesh.


```bash
kubectl -n istio-system port-forward svc/kiali 20001:20001
```


Access at: http://localhost:20001