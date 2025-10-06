# Oveeview

Istio is a service mesh that manages how microservices share data with each other. It adds observability, traffic control, and security to Kubernetes environments.


### Key components
- **Pilot** – controls traffic routing.
- **Mixer** – handles policies and telemetry.
- **Citadel** – manages security certificates.
- **Envoy proxy** – sidecar container that manages traffic for each pod.


### Benefits
- Fine control of service communication.
- Traffic splitting, retries, and mirroring.
- mTLS for encryption.
- Metrics and tracing integration.

