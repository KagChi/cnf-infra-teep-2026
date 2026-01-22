## Install Longhorn
```bash
helm upgrade --install longhorn longhorn/longhorn --namespace longhorn-system --create-namespace --version 1.10.0 -f values.yaml
```

# CloudNative-PG
```bash
helm upgrade --install cnpg --namespace cnpg-system --create-namespace cnpg/cloudnative-pg
```

# Kubernetes Replicator
```bash
helm upgrade --install --namespace replicator-system --create-namespace kubernetes-replicator mittwald/kubernetes-replicator
```

# Cert-Manager
```bash
helm install cert-manager oci://quay.io/jetstack/charts/cert-manager --version v1.18.2 --namespace cert-manager --create-namespace --set crds.enabled=true
```

# NGINX Ingress Controller
```bash
helm upgrade --install ingress-nginx ingress-nginx --repo https://kubernetes.github.io/ingress-nginx --namespace ingress-nginx --create-namespace
```

# FluxCD
```bash
$env:GITHUB_TOKEN="github_pat"; flux bootstrap github --components-extra image-reflector-controller,image-automation-controller --token-auth --owner=kagchi --repository=cnf-infra-teep-2026 --branch=main --path=clusters/demon
```