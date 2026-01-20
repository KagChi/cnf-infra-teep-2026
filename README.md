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

# FluxCD
```bash
$env:GITHUB_TOKEN="github_pat"; flux bootstrap github --components-extra image-reflector-controller,image-automation-controller --token-auth --owner=kagchi --repository=cnf-infra-teep-2026 --branch=main --path=clusters/demon
```