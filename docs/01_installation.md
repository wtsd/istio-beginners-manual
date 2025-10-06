# Installation

## 1. Install Istio CLI

Based on https://istio.io/latest/docs/setup/additional-setup/download-istio-release/

```bash
curl -L https://istio.io/downloadIstio | sh -
cd istio-*
export PATH=$PWD/bin:$PATH
```


## 2. Deploy Istio into cluster

Based on https://istio.io/latest/docs/setup/install/istioctl/

```bash

#istioctl install --set meshConfig.accessLogFile=/dev/stdout

istioctl install --set profile=demo
kubectl label namespace default istio-injection=enabled
```


## 3. Verify installation

Checking if injection worked: https://istio.io/latest/docs/ops/diagnostic-tools/check-inject/

```bash
istioctl verify-install
kubectl get pods -n istio-system
#Expected output: all pods should be in Running state.

istioctl experimental check-inject -n <namespace> <pod-name>
```

